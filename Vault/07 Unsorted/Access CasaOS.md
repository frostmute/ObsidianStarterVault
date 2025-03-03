---
banner: 03 - MEDIA & FILES/BANNERS/pixel-banner-image-5.png
---

```embed
url: https://github.com/IceWhaleTech/CasaOS/issues/1074
title: "[Feedback][Feature Request] SSL/TLS Support for CasaOS.local · Issue #1074 · IceWhaleTech/CasaOS"
description: "Description Forgive me if my Google-fu isn't up to par, but I haven't been able to find a way to set up SSL/TLS for http://casaos.local > https://casaos.local. It would be nice to have, at a minimu..."
host: github.com
favicon: https://github.githubassets.com/favicons/favicon.svg
image: https://opengraph.githubassets.com/b592b89e8c33234b8a76f608be04c20f5a48dfe11ffb410fb8aaf7fb98cd6d66/IceWhaleTech/CasaOS/issues/1074
```

While it is doable, it isn't trivial as casaos-gateway isn't running behind a reverse proxy (nginx, apache, caddy, traefik), but rather is exposed to port 80 directly

Looking at the /etc/casaos/gateway.ini file, [I don't see any options for](https://github.com/search?q=repo%3AIceWhaleTech%2FCasaOS-Gateway+tls&type=code) `tls` or `ssl`.

The one downside to doing this with nginx is that the `tailscale cert` only generates 90 day certificates. Caddy [will handle auto renewing](https://tailscale.com/blog/caddy) the cert

This works on ubuntu. Note that you do need to change the port from 80 to 81 so caddy and casaos don't collide.

NOTE: Some Apps don't work behind caddy, I haven't figured out why yet.

# Generate Tailscale Cert
NAME="$(tailscale status --json | jq '.Self.DNSName | .[:-1]' -r)"
tailscale cert "${NAME}"

# Install Caddy on Debian
sudo apt install -y debian-keyring debian-archive-keyring apt-transport-https
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/gpg.key' | sudo gpg --dearmor -o /usr/share/keyrings/caddy-stable-archive-keyring.gpg
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/debian.deb.txt' | sudo tee /etc/apt/sources.list.d/caddy-stable.list
sudo apt update
sudo apt install caddy

# Change Casaos to Listen on Port 81
sed -i 's/80/81/g' /etc/casaos/gateway.ini
service casaos-gateway restart

# Backup Caddy Config
mv /etc/caddy/Caddyfile /etc/caddy/Caddyfile.bak

echo "${NAME}:443 {
		reverse_proxy 127.0.0.1:81
}" > /etc/caddy/Caddyfile

# This May not Be Required on Some OS's
echo "TS_PERMIT_CERT_UID=caddy" >> /etc/default/tailscaled

# Start Caddy
caddy run -c /etc/caddy/Cadyfile #TODO: Get systemd working
