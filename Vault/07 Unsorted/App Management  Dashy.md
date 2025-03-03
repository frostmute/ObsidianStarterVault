---
feature: "![[../03 - MEDIA & FILES/8af3f5cf45d0c3fdfdd689abfe98dc55_MD5.png]]"
banner: "[[../03 - MEDIA & FILES/8af3f5cf45d0c3fdfdd689abfe98dc55_MD5.png]]"
---

---

created: 2024-07-07
source: <https://dashy.to/docs/management/#providing-assets>
category:

- "[[../00 - CATEGORIES/Clippings](../00%20-%20CATEGORIES/Clippings.md)"
	cssclasses:
- obsidian-banner
- page-grid
- pen-white
- dashboard
	poster: " ![poster](../03%20-%20MEDIA%20&%20FILES/8af3f5cf45d0c3fdfdd689abfe98dc55_MD5.png)"
	tags:
- clippings
- dashboards
- selfhosted
- software
- webapp


---

 ![banner](../03%20-%20MEDIA%20&%20FILES/8af3f5cf45d0c3fdfdd689abfe98dc55_MD5.png)

```meta-bind-button
label: Fold All
icon: ""
hidden: false
class: ""
tooltip: ""
id: "001"
style: primary
actions:
  - type: command
    command: editor:fold-all
```

```meta-bind-button
label: Un-Fold All
icon: ""
hidden: false
class: ""
tooltip: ""
id: "002"
style: primary
actions:
  - type: command
    command: editor:unfold-all
```

***

```cardlink
url: https://dashy.to/docs/management/#providing-assets
title: "App Management | Dashy"
description: "The following article is a primer on managing self-hosted apps. It covers everything from keeping the Dashy (or any other app) up-to-date, secure, backed up, to other topics like auto-starting, monitoring, log management, web server configuration and using custom domains."
host: dashy.to
image: 
```

***

# App Management

_The following article is a primer on managing self-hosted apps. It covers everything from keeping the Dashy (or any other app) up-to-date, secure, backed up, to other topics like auto-starting, monitoring, log management, web server configuration and using custom domains._

## Contents\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#contents "Direct Link to heading"\]\]

- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#providing-assets\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#running-commands\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#healthchecks\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#logs-and-performance\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#auto-starting-at-system-boot\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#updating\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#backing-up\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#scheduling\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#ssl-certificates\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#authentication\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#managing-containers-with-docker-compose\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#passing-in-environmental-variables\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#setting-headers\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#remote-access\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#custom-domain\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#container-security\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#web-server-configuration\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#running-a-modified-version-of-the-app\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#building-your-own-container\]\]


***

## Providing Assets\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#providing-assets "Direct Link to heading"\]\]

Although not essential, you will most likely want to provide several assets to your running app.

This is easy to do using [Docker Volumes](https://docs.docker.com/storage/volumes/), which lets you share a file or directory between your host system, and the container. Volumes are specified in the Docker run command, or Docker compose file, using the `--volume` or `-v` flags. The value of which consists of the path to the file / directory on your host system, followed by the destination path within the container. Fields are separated by a colon (`:`), and must be in the correct order. For example: `-v ~/alicia/my-local-conf.yml:/app/user-data/conf.yml`

In Dashy, commonly configured resources include:

- `./user-data/conf.yml` - Your main application config file
- `./public/item-icons` - A directory containing your own icons. This allows for offline access, and better performance than fetching from a CDN
- Also within `./public` you'll find standard website assets, including `favicon.ico`, `manifest.json`, `robots.txt`, etc. There's no need to pass these in, but you can do so if you wish
- `/src/styles/user-defined-themes.scss` - A stylesheet for applying custom CSS to your app. You can also write your own themes here.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Running Commands\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#running-commands "Direct Link to heading"\]\]

If you're running an app in Docker, then commands will need to be passed to the container to be executed. This can be done by preceding each command with `docker exec -it [container-id]`, where container ID can be found by running `docker ps`. For example `docker exec -it 26c156c467b4 yarn build`. You can also enter the container, with `docker exec -it [container-id] /bin/ash`, and navigate around it with normal Linux commands.

Dashy has several commands that can be used for various tasks, you can find a list of these either in the \[\[https://dashy.to/docs/developing#project-commands\]\], or by looking at the \[\[https://github.com/Lissy93/dashy/blob/master/package.json#L5\]\]. These can be used by running `yarn [command-name]`.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Healthchecks\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#healthchecks "Direct Link to heading"\]\]

Healthchecks are configured to periodically check that Dashy is up and running correctly on the specified port. By default, the health script is called every 5 minutes, but this can be modified with the `--health-interval` option. You can check the current container health with: `docker inspect --format "{{json .State.Health }}" [container-id]`, and a summary of health status will show up under `docker ps`. You can also manually request the current application status by running `docker exec -it [container-id] yarn health-check`. You can disable healthchecks altogether by adding the `--no-healthcheck` flag to your Docker run command.

To restart unhealthy containers automatically, check out [Autoheal](https://hub.docker.com/r/willfarrell/autoheal/). This image watches for unhealthy containers, and automatically triggers a restart. (This is a stand in for Docker's `--exit-on-unhealthy` that was proposed, but [not merged](https://github.com/moby/moby/pull/22719)). There's also [Deunhealth](https://github.com/qdm12/deunhealth), which is super light-weight, and doesn't require network access.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token function" style="color: rgb(80, 250, 123);">docker</span><span class="token plain"> run -d </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    --name autoheal </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    --restart</span><span class="token operator">=</span><span class="token plain">always </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    -e </span><span class="token assign-left variable" style="color: rgb(189, 147, 249); font-style: italic;">AUTOHEAL_CONTAINER_LABEL</span><span class="token operator">=</span><span class="token plain">all </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    -v /var/run/docker.sock:/var/run/docker.sock </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    willfarrell/autoheal</span></span>
```

Copy

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Logs and Performance\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#logs-and-performance "Direct Link to heading"\]\]

### Container Logs\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#container-logs "Direct Link to heading"\]\]

You can view logs for a given Docker container with `docker logs [container-id]`, add the `--follow` flag to stream the logs. For more info, see the [Logging Documentation](https://docs.docker.com/config/containers/logging/). There's also [Dozzle](https://dozzle.dev/), a useful tool, that provides a web interface where you can stream and query logs from all your running containers from a single web app.

### Container Performance\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#container-performance "Direct Link to heading"\]\]

You can check the resource usage for your running Docker containers with `docker stats` or `docker stats [container-id]`. For more info, see the [Stats Documentation](https://docs.docker.com/engine/reference/commandline/stats/). There's also [cAdvisor](https://github.com/google/cadvisor), a useful web app for viewing and analyzing resource usage and performance of all your running containers.

### Management Apps\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#management-apps "Direct Link to heading"\]\]

You can also view logs, resource usage and other info as well as manage your entire Docker workflow in third-party Docker management apps. For example [Portainer](https://github.com/portainer/portainer) an all-in-one open source management web UI for Docker and Kubernetes, or [LazyDocker](https://github.com/jesseduffield/lazydocker) a terminal UI for Docker container management and monitoring.

### Advanced Logging and Monitoring\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#advanced-logging-and-monitoring "Direct Link to heading"\]\]

Docker supports using [Prometheus](https://prometheus.io/) to collect logs, which can then be visualized using a platform like [Grafana](https://grafana.com/). For more info, see [this guide](https://docs.docker.com/config/daemon/prometheus/). If you need to route your logs to a remote syslog, then consider using [logspout](https://github.com/gliderlabs/logspout). For enterprise-grade instances, there are managed services, that make monitoring container logs and metrics very easy, such as [Sematext](https://sematext.com/blog/docker-container-monitoring-with-sematext/) with [Logagent](https://github.com/sematext/logagent-js).

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Auto-Starting at System Boot\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#auto-starting-at-system-boot "Direct Link to heading"\]\]

You can use Docker's <https://docs.docker.com/engine/reference/run/#restart-policies---restart> to instruct the container to start after a system reboot, or restart after a crash. Just add the `--restart=always` flag to your Docker compose script or Docker run command. For more information, see the docs on [Starting Containers Automatically](https://docs.docker.com/config/containers/start-containers-automatically/).

For Podman, you can use `systemd` to create a service that launches your container, [the docs](https://podman.io/blogs/2018/09/13/systemd.html) explains things further. A similar approach can be used with Docker, if you need to start containers after a reboot, but before any user interaction.

To restart the container after something within it has crashed, consider using `docker-autoheal` by @willfarrell, a service that monitors and restarts unhealthy containers. For more info, see the \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#healthchecks\]\] section above.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Updating\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#updating "Direct Link to heading"\]\]

Dashy is under active development, so to take advantage of the latest features, you may need to update your instance every now and again.

### Updating Docker Container\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#updating-docker-container "Direct Link to heading"\]\]


1. Pull latest image: `docker pull lissy93/dashy:latest`
2. Kill off existing container
	 - Find container ID: `docker ps`
	 - Stop container: `docker stop [container_id]`
	 - Remove container: `docker rm [container_id]`
3. Spin up new container: `docker run [params] lissy93/dashy`

### Automatic Docker Updates\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#automatic-docker-updates "Direct Link to heading"\]\]

You can automate the above process using [Watchtower](https://github.com/containrrr/watchtower). Watchtower will watch for new versions of a given image on Docker Hub, pull down your new image, gracefully shut down your existing container and restart it with the same options that were used when it was deployed initially.

To get started, spin up the watchtower container:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token function" style="color: rgb(80, 250, 123);">docker</span><span class="token plain"> run -d </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  --name watchtower </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  -v /var/run/docker.sock:/var/run/docker.sock </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  containrrr/watchtower</span></span>
```

Copy

For more information, see the [Watchtower Docs](https://containrrr.dev/watchtower/)

### Updating Dashy from Source\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#updating-dashy-from-source "Direct Link to heading"\]\]

Stop your current instance of Dashy, then navigate into the source directory. Pull down the latest code, with `git pull origin master`, then update dependencies with `yarn`, rebuild with `yarn build`, and start the server again with `yarn start`.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Backing Up\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#backing-up "Direct Link to heading"\]\]

### Backing Up Containers\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#backing-up-containers "Direct Link to heading"\]\]

You can make a backup of any running container really easily, using `docker commit` and save it with `docker export`, to do so:

- First find the container ID, you can do this with `docker container ls`
- Now to create the snapshot, just run `docker commit -p [container-id] my-backup`
- Finally, to save the backup locally, run `docker save -o ~/dashy-backup.tar my-backup`
- If you want to push this to a container registry, run `docker push my-backup:latest`

Note that this will not include any data in docker volumes, and the process here is a bit different. Since these files exist on your host system, if you have an existing backup solution implemented, you can incorporate and volume files within that system.

### Backing Up Volumes\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#backing-up-volumes "Direct Link to heading"\]\]

[offen/docker-volume-backup](https://github.com/offen/docker-volume-backup) is a useful tool for periodic Docker volume backups, to any S3-compatible storage provider. It's run as a light-weight Docker container, and is easy to setup, and also supports GPG-encryption, email notification, and routing away older backups.

To get started, create a docker-compose similar to the example below, and then start the container. For more info, check out their [documentation](https://github.com/offen/docker-volume-backup), which is very clear.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token key atrule">version</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token string" style="color: rgb(255, 121, 198);">'3'</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"></span><span class="token key atrule">services</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  </span><span class="token key atrule">backup</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">image</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> offen/docker</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">volume</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">backup</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain">latest</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">environment</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">BACKUP_CRON_EXPRESSION</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token string" style="color: rgb(255, 121, 198);">"0 * * * *"</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">BACKUP_PRUNING_PREFIX</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> backup</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">BACKUP_RETENTION_DAYS</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token number">7</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">AWS_BUCKET_NAME</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> backup</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">bucket</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">AWS_ACCESS_KEY_ID</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> AKIAIOSFODNN7EXAMPLE</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">AWS_SECRET_ACCESS_KEY</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">volumes</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> data</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain">/backup/my</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">app</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">backup</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain">ro</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> /var/run/docker.sock</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain">/var/run/docker.sock</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain">ro</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"></span><span class="token key atrule">volumes</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  data</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span></span>
```

Copy

It's worth noting that this process can also be done manually, using the following commands:

Backup:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token function" style="color: rgb(80, 250, 123);">docker</span><span class="token plain"> run --rm -v some_volume:/volume -v /tmp:/backup alpine </span><span class="token function" style="color: rgb(80, 250, 123);">tar</span><span class="token plain"> -cjf /backup/some_archive.tar.bz2 -C /volume ./</span></span>
```

Copy

Restore:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token function" style="color: rgb(80, 250, 123);">docker</span><span class="token plain"> run --rm -v some_volume:/volume -v /tmp:/backup alpine </span><span class="token function" style="color: rgb(80, 250, 123);">sh</span><span class="token plain"> -c </span><span class="token string" style="color: rgb(255, 121, 198);">"rm -rf /volume/* /volume/..?* /volume/.[!.]* ; tar -C /volume/ -xjf /backup/some_archive.tar.bz2"</span></span>
```

Copy

### Dashy-Specific Backup\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#dashy-specific-backup "Direct Link to heading"\]\]

All configuration and dashboard settings are stored in your `user-data/conf.yml` file. If you provide additional assets (like icons, fonts, themes, etc), these will also live in the `user-data` directory. So to backup all Dashy data, this is the only directory you need to backup.

Since Dashy is open source, there shouldn't be any need to backup the main container.

Dashy also has a built-in cloud backup feature, which is free for personal users, and will let you make and restore fully encrypted backups of your config directly through the UI. To learn more, see the [Cloud Backup Docs](https://dashy.to/docs/backup-restore)

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Scheduling\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#scheduling "Direct Link to heading"\]\]

If you need to periodically schedule the running of a given command on Dashy (or any other container), then a useful tool for doing so it [ofelia](https://github.com/mcuadros/ofelia). This runs as a Docker container and is really useful for things like backups, logging, updating, notifications, etc. Crons are specified using Go's crontab format, and a useful tool for visualizing this is [crontab.guru](https://crontab.guru/). This can also be done natively with Alpine: `docker run -it alpine ls /etc/periodic`. I recommend combining this with [healthchecks](https://github.com/healthchecks/healthchecks) for easy monitoring of jobs, and failure notifications.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## SSL Certificates\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#ssl-certificates "Direct Link to heading"\]\]

Enabling HTTPS with an SSL certificate is recommended, especially if you are hosting Dashy anywhere other than your home. This will ensure that all traffic is encrypted in transit.

### Auto-SSL\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#auto-ssl "Direct Link to heading"\]\]

If you are using [NGINX Proxy Manager](https://nginxproxymanager.com/), then SSL is supported out of the box. Once you've added your proxy host and web address, then set the scheme to HTTPS, then under the SSL Tab select "Request a new SSL certificate" and follow the on-screen instructions.

If you're hosting Dashy behind Cloudflare, then they offer [free and easy SSL](https://www.cloudflare.com/en-gb/learning/ssl/what-is-an-ssl-certificate/)- all you need to do is enable it under the SSL/TLS tab. Or if you are using shared hosting, you may find [this tutorial](https://www.sitepoint.com/a-guide-to-setting-up-lets-encrypt-ssl-on-shared-hosting/) helpful.

### Getting a Self-Signed SSL Certificate\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#getting-a-self-signed-ssl-certificate "Direct Link to heading"\]\]

[Let's Encrypt](https://letsencrypt.org/docs/) is a global Certificate Authority, providing free SSL/TLS Domain Validation certificates in order to enable secure HTTPS access to your website. They have good browser/ OS [compatibility](https://letsencrypt.org/docs/certificate-compatibility/) with their ISRG X1 and DST CA X3 root certificates, support [Wildcard issuance](https://community.letsencrypt.org/t/acme-v2-production-environment-wildcards/55578) done via ACMEv2 using the DNS-01 and have [Multi-Perspective Validation](https://letsencrypt.org/2020/02/19/multi-perspective-validation.html). Let's Encrypt provide [CertBot](https://certbot.eff.org/) an easy app for generating and setting up an SSL certificate.

This process can be automated, using something like the [Docker-NGINX-Auto-SSL Container](https://github.com/Valian/docker-nginx-auto-ssl) to generate and renew certificates when needed.

If you're not so comfortable on the command line, then you can use a tool like [SSL For Free](https://www.sslforfree.com/) or [ZeroSSL](https://zerossl.com/) to generate your cert. They also provide step-by-step setup instructions for most platforms.

### Passing a Self-Signed Certificate to Dashy\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#passing-a-self-signed-certificate-to-dashy "Direct Link to heading"\]\]

Once you've generated your SSL cert, you'll need to pass it to Dashy. This can be done by specifying the paths to your public and private keys using the `SSL_PRIV_KEY_PATH` and `SSL_PUB_KEY_PATH` environmental variables. Or if you're using Docker, then just pass public + private SSL keys in under `/etc/ssl/certs/dashy-pub.pem` and `/etc/ssl/certs/dashy-priv.key` respectively, e.g:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token function" style="color: rgb(80, 250, 123);">docker</span><span class="token plain"> run -d </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  -p </span><span class="token number">8080</span><span class="token plain">:8080 </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  -v ~/my-private-key.key:/etc/ssl/certs/dashy-priv.key:ro </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  -v ~/my-public-key.pem:/etc/ssl/certs/dashy-pub.pem:ro </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  lissy93/dashy:latest</span></span>
```

Copy

By default the SSL port is `443` within a Docker container, or `4001` if running on bare metal, but you can override this with the `SSL_PORT` environmental variable.

Once everything is setup, you can verify your site is secured using a tool like [SSL Checker](https://www.sslchecker.com/sslchecker).

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Authentication\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#authentication "Direct Link to heading"\]\]

Dashy natively supports secure authentication using KeyCloak. There is also a Simple Auth feature that doesn't require any additional setup. Usage instructions for both, as well as alternative auth methods, has now moved to the **[Authentication Docs](https://dashy.to/docs/authentication)** page.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Managing Containers with Docker Compose\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#managing-containers-with-docker-compose "Direct Link to heading"\]\]

When you have a lot of containers, it quickly becomes hard to manage with `docker run` commands. The solution to this is [docker compose](https://docs.docker.com/compose/), a handy tool for defining all a containers run settings in a single YAML file, and then spinning up that container with a single short command - `docker compose up`. A good example of which can be seen in [@abhilesh's docker compose collection](https://github.com/abhilesh/self-hosted_docker_setups).

You can use Dashy's default `docker-compose.yml` file as a template, and modify it according to your needs.

An example Docker compose, using the default base image from DockerHub, might look something like this:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token punctuation" style="color: rgb(248, 248, 242);">---</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"></span><span class="token key atrule">version</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token string" style="color: rgb(255, 121, 198);">"3.8"</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"></span><span class="token key atrule">services</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  </span><span class="token key atrule">dashy</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">container_name</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> Dashy</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">image</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> lissy93/dashy</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">volumes</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> /root/my</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">config.yml</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain">/app/user</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">data/conf.yml</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">ports</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> 4000</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token number">8080</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">environment</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> BASE_URL=/my</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">dashboard</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">restart</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> unless</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">stopped</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">healthcheck</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">test</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token punctuation" style="color: rgb(248, 248, 242);">[</span><span class="token string" style="color: rgb(255, 121, 198);">'CMD'</span><span class="token punctuation" style="color: rgb(248, 248, 242);">,</span><span class="token plain"> </span><span class="token string" style="color: rgb(255, 121, 198);">'node'</span><span class="token punctuation" style="color: rgb(248, 248, 242);">,</span><span class="token plain"> </span><span class="token string" style="color: rgb(255, 121, 198);">'/app/services/healthcheck'</span><span class="token punctuation" style="color: rgb(248, 248, 242);">]</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">interval</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> 1m30s</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">timeout</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> 10s</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">retries</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token number">3</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      </span><span class="token key atrule">start_period</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> 40s</span></span>
```

Copy

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Passing in Environmental Variables\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#passing-in-environmental-variables "Direct Link to heading"\]\]

With Docker, you can define environmental variables under the `environment` section of your Docker compose file. Environmental variables are used to configure high-level settings, usually before the config file has been read. For a list of all supported env vars in Dashy, see <https://dashy.to/docs/developing#environmental-variables>, or the default `.env` file.

A common use case, is to run Dashy under a sub-page, instead of at the root of a URL (e.g. `https://my-homelab.local/dashy` instead of `https://dashy.my-homelab.local`). In this use-case, you'd specify the `BASE_URL` variable in your compose file.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token key atrule">environment</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> BASE_URL=/dashy</span></span>
```

Copy

You can also do the same thing with the docker run command, using the <https://docs.docker.com/engine/reference/commandline/run/#set-environment-variables--e---env---env-file> flag. If you've got many environmental variables, you might find it useful to put them in a `.env` file. Similarly, for Docker run you can use <https://docs.docker.com/engine/reference/commandline/run/#set-environment-variables--e---env---env-file> if you'd like to pass in a file containing all your environmental variables.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Setting Headers\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#setting-headers "Direct Link to heading"\]\]

Any external requests made to a different origin (app/ service under a different domain) will be blocked if the correct headers are not specified. This is known as [Cross-Origin Resource Sharing](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) (CORS) and is a security feature built into modern browsers.

If you see a CORS error in your console, this can be easily fixed by setting the correct headers. This is not a bug with Dashy, so please don't raise it as a bug!

### Example Headers\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#example-headers "Direct Link to heading"\]\]

- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#caddy\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#nginx\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#traefik\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#haproxy\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#apache\]\]

_The following section briefly outlines how you can set headers for common web proxies/ servers. More info can be found in the documentation for the proxy that you are using, or in the [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)._

These examples are using:

- `Access-Control-Allow-Origin` header, but depending on what type of content you are enabling, this will vary. For example, to allow a site to be loaded in an iframe (for the modal or workspace views) you would use `X-Frame-Options`.
- The domain root (`/`), if your're hosting from a sub-page, replace that with your path.
- A wildcard (`*`), which would allow access from traffic on any domain, this is discouraged, and you should replace it with the URL where you are hosting Dashy. Note that for requests that transport sensitive info, like credentials (e.g. Keycloak login), the wildcard is <https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#requests_with_credentials> and will be blocked.

#### Caddy\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#caddy "Direct Link to heading"\]\]

> See [Caddy ](https://caddyserver.com/docs/caddyfile/directives/header)`header` docs for more info.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">headers / {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  Access-Control-Allow-Origin *</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">}</span></span>
```

Copy

#### NGINX\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#nginx "Direct Link to heading"\]\]

> See [NGINX ](https://nginx.org/en/docs/http/ngx_http_headers_module.html)`ngx_http_headers_module` docs for more info.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">location / {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  add_header Access-Control-Allow-Origin *;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">}</span></span>
```

Copy

Note this can also be done through the UI, using NGINX Proxy Manager.

#### Traefik\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#traefik "Direct Link to heading"\]\]

> See <https://doc.traefik.io/traefik/middlewares/http/headers/#cors-headers> for more info.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">labels:</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  - "traefik.http.middlewares.testheader.headers.accesscontrolallowmethods=GET,OPTIONS,PUT"</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  - "traefik.http.middlewares.testheader.headers.accesscontrolalloworiginlist=https://foo.bar.org,https://example.org"</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  - "traefik.http.middlewares.testheader.headers.accesscontrolmaxage=100"</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  - "traefik.http.middlewares.testheader.headers.addvaryheader=true"</span></span>
```

Copy

#### HAProxy\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#haproxy "Direct Link to heading"\]\]

> See [HAProxy Rewrite Response Docs](https://www.haproxy.com/documentation/hapee/latest/traffic-routing/rewrites/rewrite-responses/) for more info.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">/</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">   http-response add-header Access-Control-Allow-Origin *</span></span>
```

Copy

#### Apache\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#apache "Direct Link to heading"\]\]

> See [Apache ](https://httpd.apache.org/docs/current/mod/mod_headers.html)`mode_headers` docs for more info.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">Header always set Access-Control-Allow-Origin "*"</span></span>
```

Copy

#### Squid\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#squid "Direct Link to heading"\]\]

> See [Squid ](http://www2.gr.squid-cache.org/Doc/config/request_header_access/)`request_header_access` docs for more info.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">request_header_access Authorization allow all</span></span>
```

Copy

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Remote Access\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#remote-access "Direct Link to heading"\]\]

- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#wireguard\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#reverse-ssh-tunnel\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#tcp-tunnel\]\]

### WireGuard\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#wireguard "Direct Link to heading"\]\]

Using a VPN is one of the easiest ways to provide secure, full access to your local network from remote locations. [WireGuard](https://www.wireguard.com/) is a reasonably new open source VPN protocol, that was designed with ease of use, performance and security in mind. Unlike OpenVPN, it doesn't need to recreate the tunnel whenever connection is dropped, and it's also much easier to setup, using shared keys instead.

- **Install Wireguard** - See the [Install Docs](https://www.wireguard.com/install/) for download links + instructions
	- On Debian-based systems, it's `sudo apt install wireguard`
- **Generate a Private Key** - Run `wg genkey` on the Wireguard server, and copy it to somewhere safe for later
- **Create Server Config** - Open or create a file at `/etc/wireguard/wg0.conf` and under `[Interface]` add the following (see example below):
	- `Address` - as a subnet of all desired IPs
	- `PrivateKey` - that you just generated
	- `ListenPort` - Default is `51820`, but can be anything
- **Get Client App** - Download the [WG client app](https://www.wireguard.com/install/) for your platform (Linux, Windows, MacOS, Android or iOS are all supported)
- **Create new Client Tunnel** - On your client app, there should be an option to create a new tunnel, when doing so a client private key will be generated (but if not, use the `wg genkey` command again), and keep it somewhere safe. A public key will also be generated, and this will go in our saver config
- **Add Clients to Server Config** - Head back to your `wg0.conf` file on the server, create a `[Peer]` section, and populate the following info
	- `AllowedIPs` - List of IP address inside the subnet, the client should have access to
	- `PublicKey` - The public key for the client you just generated
- **Start the Server** - You can now start the WG server, using: `wg-quick up wg0` on your server
- **Finish Client Setup** - Head back to your client device, and edit the config file, leave the private key as is, and add the following fields:
	- `PublicKey` - The public key of the server
	- `Address` - This should match the `AllowedIPs` section on the servers config file
	- `DNS` - The DNS server that'll be used when accessing the network through the VPN
	- `Endpoint` - The hostname or IP + Port where your WG server is running (you may need to forward this in your firewall's settings)
- **Done** - Your clients should now be able to connect to your WG server :) Depending on your networks firewall rules, you may need to port forward the address of your WG server

#### **Example Server Config**\[\[https://dashy.to/docs/management/#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#example-server-config "Direct Link to heading"\]\]

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Server file</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">[Interface]</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Which networks does my interface belong to? Notice: /24 and /64</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">Address = 10.5.0.1/24, 2001:470:xxxx:xxxx::1/64</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">PrivateKey = xxx</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">ListenPort = 51820</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Peer 1</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">[Peer]</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">PublicKey = xxx</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Which source IPs can I expect from that peer? Notice: /32 and /128</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">AllowedIps = 10.5.0.35/32, 2001:470:xxxx:xxxx::746f:786f/128</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Peer 2</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">[Peer]</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">PublicKey = xxx</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Which source IPs can I expect from that peer? This one has a LAN which can</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># access hosts/jails without NAT.</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Peer 2 has a single IP address inside the VPN: it's 10.5.0.25/32</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">AllowedIps = 10.5.0.25/32,10.21.10.0/24,10.21.20.0/24,10.21.30.0/24,10.31.0.0/24,2001:470:xxxx:xxxx::ca:571e/128</span></span>
```

Copy

#### **Example Client Config**\[\[https://dashy.to/docs/management/#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#example-client-config "Direct Link to heading"\]\]

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">[Interface]</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Which networks does my interface belong to? Notice: /24 and /64</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">Address = 10.5.0.35/24, 2001:470:xxxx:xxxx::746f:786f/64</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">PrivateKey = xxx</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Server</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">[Peer]</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">PublicKey = xxx</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># I want to route everything through the server, both IPv4 and IPv6. All IPs are</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># thus available through the Server, and I can expect packets from any IP to</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># come from that peer.</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">AllowedIPs = 0.0.0.0/0, ::0/0</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Where is the server on the internet? This is a public address. The port</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># (:51820) is the same as ListenPort in the [Interface] of the Server file above</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">Endpoint = 1.2.3.4:51820</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"># Usually, clients are behind NAT. to keep the connection running, keep alive.</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">PersistentKeepalive = 15</span></span>
```

Copy

A useful tool for getting WG setup is [Algo](https://github.com/trailofbits/algo). It includes scripts and docs which cover almost all devices, platforms and clients, and has best practices implemented, and security features enabled. All of this is better explained in [this blog post](https://blog.trailofbits.com/2016/12/12/meet-algo-the-vpn-that-works/).

### Reverse SSH Tunnel\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#reverse-ssh-tunnel "Direct Link to heading"\]\]

SSH (or [Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell)) is a secure tunnel that allows you to connect to a remote host. Unlike the VPN methods, an SSH connection does not require an intermediary, and will not be affected by your IP changing. However it only allows you to access a single service at a time. SSH was really designed for terminal access, but because of the latter mentioned benefits it's useful to setup, as a fallback option.

Directly SSH'ing into your home, would require you to open a port (usually 22), which would be terrible for security, and is not recommended. However a reverse SSH connection is initiated from inside your network. Once the connection is established, the port is redirected, allowing you to use the established connection to SSH into your home network.

The issue you've probably spotted, is that most public, corporate, and institutional networks will block SSH connections. To overcome this, you'd have to establish a server outside of your homelab that your homelab's device could SSH into to establish the reverse SSH connection. You can then connect to that remote server (the _mothership_), which in turn connects to your home network.

Now all of this is starting to sound like quite a lot of work, but this is where services like [remot3.it](https://remote.it/) come in. They maintain the intermediary mothership server, and create the tunnel service for you. It's free for personal use, secure and easy. There are several similar services, such as [RemoteIoT](https://remoteiot.com/), or you could create your own on a cloud VPS (see [this tutorial](https://gist.github.com/nileshtrivedi/4c615e8d3c1bf053b0d31176b9e69e42) for more info on that).

Before getting started, you'll need to head over to <https://app.remote.it/auth/#/sign-up> and create an account.

Then setup your local device:


1. If you haven't already done so, you'll need to enable and configure SSH.
	 - This is out-of-scope of this article, but I've explained it in detail in <https://notes.aliciasykes.com/22798/my-server-setup#configure-ssh>.
2. Download the [Remote.it](http://Remote.it) install script from their [GitHub](https://github.com/remoteit/installer)
	 - `curl -LkO https://raw.githubusercontent.com/remoteit/installer/master/scripts/auto-install.sh`
3. Make it executable, with `chmod +x ./auto-install.sh`, and then run it with `sudo ./auto-install.sh`
4. Finally, configure your device, by running `sudo connectd_installer` and following the on-screen instructions

And when you're ready to connect to it:


1. Login to [app.remote.it](https://app.remote.it/), and select the name of your device
2. You should see a list of running services, click SSH
3. You'll then be presented with some SSH credentials that you can now use to securely connect to your home, via the [Remote.it](http://Remote.it) servers

Done :)

### TCP Tunnel\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#tcp-tunnel "Direct Link to heading"\]\]

If you're running Dashy on your local network, behind a firewall, but need to temporarily share it with someone external, this can be achieved quickly and securely using [Ngrok](https://ngrok.com/). It's basically a super slick, encrypted TCP tunnel that provides an internet-accessible address that anyone use to access your local service, from anywhere.

To get started, [Download](https://ngrok.com/download) and install Ngrok for your system, then just run \`ngrok http <https://ngrok.com/docs#http-local-https>, specify the full local url/ ip including the protocol.

Some Ngrok features require you to be authenticated, you can [create a free account](https://dashboard.ngrok.com/signup) and generate a token in [your dashboard](https://dashboard.ngrok.com/auth/your-authtoken), then run `ngrok authtoken [token]`.

It's recommended to use authentication for any publicly accessible service. Dashy has an [Auth](https://dashy.to/docs/authentication) feature built in, but an even easier method it to use the <https://ngrok.com/docs#http-auth> switch. E.g. `ngrok http -auth="username:password123" 8080`

By default, your web app is assigned a randomly generated ngrok domain, but you can also use your own custom domain. Under the [Domains Tab](https://dashboard.ngrok.com/endpoints/domains) of your Ngrok dashboard, add your domain, and follow the CNAME instructions. You can now use your domain, with the \[\[https://ngrok.com/docs#http-custom-domains\]\] switch, e.g.# `ngrok http -region=us -hostname=dashy.example.com 8080`. If you don't have your own domain name, you can instead use a custom sub-domain (e.g. `alicia-dashy.ngrok.io`), using the \[\[https://ngrok.com/docscustom-subdomain-names\]\] switch.

To integrate this into your docker-compose, take a look at the [gtriggiano/ngrok-tunnel](https://github.com/gtriggiano/ngrok-tunnel) container.

There's so much more you can do with Ngrok, such as exposing a directory as a file browser, using websockets, relaying requests, rewriting headers, inspecting traffic, TLS and TCP tunnels and lots more. All or which is explained in [the Documentation](https://ngrok.com/docs).

It's worth noting that Ngrok isn't the only option here, other options include: [FRP](https://github.com/fatedier/frp), [Inlets](https://inlets.dev), [Local Tunnel](https://localtunnel.me/), [TailScale](https://tailscale.com/), etc. Check out [Awesome Tunneling](https://github.com/anderspitman/awesome-tunneling) for a list of alternatives.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Custom Domain\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#custom-domain "Direct Link to heading"\]\]

- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#using-nginx\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#using-dns\]\]

### Using DNS\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#using-dns "Direct Link to heading"\]\]

For locally running services, a domain can be set up directly in the DNS records. This method is really quick and easy, and doesn't require you to purchase an actual domain. Just update your networks DNS resolver, to point your desired URL to the local IP where Dashy (or any other app) is running. For example, a line in your hosts file might look something like: `192.168.0.2 dashy.homelab.local`.

If you're using Pi-Hole, a similar thing can be done in the `/etc/dnsmasq.d/03-custom-dns.conf` file, add a line like: `address=/dashy.example.com/192.168.2.0` for each of your services.

If you're running OPNSense/ PfSense, then this can be done through the UI with Unbound, it's explained nicely in [this article](https://homenetworkguy.com/how-to/use-custom-domain-name-in-internal-network/), by Dustin Casto.

### Using NGINX\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#using-nginx "Direct Link to heading"\]\]

If you're using NGINX, then you can use your own domain name, with a config similar to the below example.

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">upstream dashy {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  server 127.0.0.1:32400;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">}</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">server {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  listen         8080;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  server_name    dashy.mydomain.com;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  # Setup SSL</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  ssl_certificate             /var/www/mydomain/sslcert.pem;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  ssl_certificate_key         /var/www/mydomain/sslkey.pem;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  ssl_protocols               TLSv1 TLSv1.1 TLSv1.2;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  ssl_ciphers                 'EECDH+AESGCM:EDH+AESGCM:AES256+EECDH:AES256+EDH';</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  ssl_session_timeout         5m;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  ssl_prefer_server_ciphers   on;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  location / {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    proxy_pass                http://dashy;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    proxy_redirect            off;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    proxy_buffering           off;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    proxy_set_header          host              $host;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    proxy_set_header          X-Real-IP         $remote_addr;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    proxy_set_header          X-Forwarded-For   $proxy_add_x_forwarded_for;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    proxy_next_upstream       error timeout     invalid_header http_500 http_502 http_503 http_504;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  }</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">}</span></span>
```

Copy

Similarly, a basic `Caddyfile` might look like:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">dashy.example.com {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    reverse_proxy / nginx:8080</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">}</span></span>
```

Copy

For more info, [this guide](https://thehomelab.wiki/books/dns-reverse-proxy/page/create-domain-records-to-point-to-your-home-server-on-cloudflare-using-nginx-progy-manager) on Setting up Domains with NGINX Proxy Manager and CloudFlare may be useful.

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Container Security\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#container-security "Direct Link to heading"\]\]

- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#keep-docker-up-to-date\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#set-resource-quotas\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#dont-run-as-root\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#specify-a-user\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#limit-capabilities\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#prevent-new-privileges-being-added\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#disable-inter-container-communication\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#dont-expose-the-docker-daemon-socket\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#use-read-only-volumes\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#set-the-logging-level\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#verify-image-before-pulling\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#specify-the-tag\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#container-security-scanning\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#registry-security\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#security-modules\]\]

### Keep Docker Up-To-Date\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#keep-docker-up-to-date "Direct Link to heading"\]\]

To prevent known container escape vulnerabilities, which typically end in escalating to root/administrator privileges, patching Docker Engine and Docker Machine is crucial. For more info, see the [Docker Installation Docs](https://docs.docker.com/engine/install/).

### Set Resource Quotas\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#set-resource-quotas "Direct Link to heading"\]\]

Docker enables you to limit resource consumption (CPU, memory, disk) on a per-container basis. This not only enhances system performance, but also prevents a compromised container from consuming a large amount of resources, in order to disrupt service or perform malicious activities. To learn more, see the [Resource Constraints Docs](https://docs.docker.com/config/containers/resource_constraints/)

For example, to run Dashy with max of 1GB ram, and max of 50% of 1 CP core: `docker run -d -p 8080:8080 --cpus=".5" --memory="1024m" lissy93/dashy:latest`

### Don't Run as Root\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#dont-run-as-root "Direct Link to heading"\]\]

Running a container with admin privileges gives it more power than it needs, and can be abused. Dashy does not need any root privileges, and Docker by default doesn't run containers as root, so providing you don't specifically type sudo, you should be all good here.

Note that if you're facing permission issues on Debian-based systems, you may need to add your user to the Docker group. First create the group: `sudo groupadd docker`, then add your (non-root) user: `sudo usermod −aG docker [my-username]`, finally `newgrp docker` to refresh.

### Specify a User\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#specify-a-user "Direct Link to heading"\]\]

One of the best ways to prevent privilege escalation attacks, is to configure the container to use an unprivileged user. This also means that any files created by the container and mounted, will be owned by the specified user (and not root), which makes things much easier.

You can specify a user, using the <https://docs.docker.com/engine/reference/run/#user>, and should include the user ID (`UID`), which can be found by running `id -u`, and the and the group ID (`GID`), using `id -g`.

With Docker run, you specify it like: `docker run --user 1000:1000 -p 8080:8080 lissy93/dashy`

Of if you're using Docker-compose, you could use an environmental variable

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token key atrule">version</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token string" style="color: rgb(255, 121, 198);">"3.8"</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"></span><span class="token key atrule">services</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  </span><span class="token key atrule">dashy</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">image</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> lissy93/dashy</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">user</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> $</span><span class="token punctuation" style="color: rgb(248, 248, 242);">{</span><span class="token plain">CURRENT_UID</span><span class="token punctuation" style="color: rgb(248, 248, 242);">}</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">ports</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token punctuation" style="color: rgb(248, 248, 242);">[</span><span class="token plain"> 4000</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token number">8080</span><span class="token plain"> </span><span class="token punctuation" style="color: rgb(248, 248, 242);">]</span></span>
```

Copy

And then to set the variable, and start the container, run: `CURRENT_UID=$(id -u):$(id -g) docker-compose up`

### Limit capabilities\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#limit-capabilities "Direct Link to heading"\]\]

Docker containers run with a subset of [Linux Kernal's Capabilities](https://man7.org/linux/man-pages/man7/capabilities.7.html) by default. It's good practice to drop privilege permissions that are not needed for any given container.

With Docker run, you can use the `--cap-drop` flag to remove capabilities, you can also use `--cap-drop=all` and then define just the required permissions using the `--cap-add` option. For a list of available capabilities, see the <https://docs.docker.com/engine/reference/run/#runtime-privilege-and-linux-capabilities>.

Note that dropping privileges and capabilities on runtime is not fool-proof, and often any leftover privileges can be used to re-escalate, see [POS36-C](https://wiki.sei.cmu.edu/confluence/display/c/POS36-C.+Observe+correct+revocation+order+while+relinquishing+privileges).

Here's an example using docker-compose, removing privileges that are not required for Dashy to run:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token key atrule">version</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token string" style="color: rgb(255, 121, 198);">"3.8"</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"></span><span class="token key atrule">services</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  </span><span class="token key atrule">dashy</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">image</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> lissy93/dashy</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">ports</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"> </span><span class="token punctuation" style="color: rgb(248, 248, 242);">[</span><span class="token plain"> 4000</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token number">8080</span><span class="token plain"> </span><span class="token punctuation" style="color: rgb(248, 248, 242);">]</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">cap_drop</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> ALL</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token key atrule">cap_add</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> CHOWN</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> SETGID</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> SETUID</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> DAC_OVERRIDE</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    </span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> NET_BIND_SERVICE</span></span>
```

Copy

### Prevent New Privileges Being Added\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#prevent-new-privileges-being-added "Direct Link to heading"\]\]

To prevent processes inside the container from getting additional privileges, pass in the `--security-opt=no-new-privileges:true` option to the Docker run command (see <https://docs.docker.com/engine/reference/run/#security-configuration>).

Run Command: `docker run --security-opt=no-new-privileges:true -p 8080:8080 lissy93/dashy`

Docker Compose

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token key atrule">security_opt</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain"></span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain"> no</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">new</span><span class="token punctuation" style="color: rgb(248, 248, 242);">-</span><span class="token plain">privileges</span><span class="token punctuation" style="color: rgb(248, 248, 242);">:</span><span class="token boolean important">true</span></span>
```

Copy

### Disable Inter-Container Communication\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#disable-inter-container-communication "Direct Link to heading"\]\]

By default Docker containers can talk to each other (using `docker0` bridged network). If you don't need this capability, then it should be disabled. This can be done with the `--icc=false` in your run command. You can learn more about how to facilitate secure communication between containers in the [Compose Networking docs](https://docs.docker.com/compose/networking/).

### Don't Expose the Docker Daemon Socket\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#dont-expose-the-docker-daemon-socket "Direct Link to heading"\]\]

Docker socket `/var/run/docker.sock` is the UNIX socket that Docker is listening to. This is the primary entry point for the Docker API. The owner of this socket is root. Giving someone access to it is equivalent to giving unrestricted root access to your host.

You should **not** enable TCP Docker daemon socket (`-H tcp://0.0.0.0:XXX`), as doing so exposes un-encrypted and unauthenticated direct access to the Docker daemon, and if the host is connected to the internet, the daemon on your computer can be used by anyone from the public internet- which is bad. If you need TCP, you should <https://docs.docker.com/engine/reference/commandline/dockerd/#daemon-socket-option> to understand how to do this more securely. Similarly, never expose `/var/run/docker.sock` to other containers as a volume, as it can be exploited.

### Use Read-Only Volumes\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#use-read-only-volumes "Direct Link to heading"\]\]

You can specify that a specific volume should be read-only by appending `:ro` to the `-v` switch. For example, while running Dashy, if we want our config to be writable, but keep all other assets protected, we would do:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token function" style="color: rgb(80, 250, 123);">docker</span><span class="token plain"> run -d </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  -p </span><span class="token number">8080</span><span class="token plain">:8080 </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  -v ~/dashy-conf.yml:/app/user-data/conf.yml </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  -v ~/dashy-icons:/app/public/item-icons:ro </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  -v ~/dashy-theme.scss:/app/src/styles/user-defined-themes.scss:ro </span><span class="token punctuation" style="color: rgb(248, 248, 242);">\</span><span class="token plain"></span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  lissy93/dashy:latest</span></span>
```

Copy

You can also prevent a container from writing any changes to volumes on your host's disk, using the `--read-only` flag. Although, for Dashy, you will not be able to write config changes to disk, when edited through the UI with this method. You could make this work, by specifying the config directory as a temp write location, with `--tmpfs /app/user-data/conf.yml` - but that this will not write the volume back to your host.

### Set the Logging Level\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#set-the-logging-level "Direct Link to heading"\]\]

Logging is important, as it enables you to review events in the future, and in the case of a compromise this will let get an idea of what may have happened. The default log level is `INFO`, and this is also the recommendation, use `--log-level info` to ensure this is set.

### Verify Image before Pulling\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#verify-image-before-pulling "Direct Link to heading"\]\]

Only use trusted images, from verified/ official sources. If an app is open source, it is more likely to be safe, as anyone can verify the code. There are also tools available for scanning containers,

Unless otherwise configured, containers can communicate among each other, so running one bad image may lead to other areas of your setup being compromised. Docker images typically contain both original code, as well as up-stream packages, and even if that image has come from a trusted source, the up-stream packages it includes may not have.

### Specify the Tag\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#specify-the-tag "Direct Link to heading"\]\]

Using fixed tags (as opposed to `:latest` ) will ensure immutability, meaning the base image will not change between builds. Note that for Dashy, the app is being actively developed, new features, bug fixes and general improvements are merged each week, and if you use a fixed version you will not enjoy these benefits. So it's up to you weather you would prefer a stable and reproducible environment, or the latest features and enhancements.

### Container Security Scanning\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#container-security-scanning "Direct Link to heading"\]\]

It's helpful to be aware of any potential security issues in any of the Docker images you are using. You can run a quick scan using Snyk on any image to output known vulnerabilities using [Docker scan](https://docs.docker.com/engine/scan/), e.g: `docker scan lissy93/dashy:latest`.

A similar product is [Trivy](https://github.com/aquasecurity/trivy), which is free an open source. First install it (with your package manager), then to scan an image, just run: `trivy image lissy93/dashy:latest`

For larger systems, RedHat [Clair](https://www.redhat.com/en/topics/containers/what-is-clair) is an app for parsing image contents and reporting on any found vulnerabilities. You run it locally in a container, and configure it with YAML. It can be integrated with Red Hat Quay, to show results on a dashboard. Most of these use static analysis to find potential issues, and scan included packages for any known security vulnerabilities.

### Registry Security\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#registry-security "Direct Link to heading"\]\]

Although over-kill for most users, you could run your own registry locally which would give you ultimate control over all images, see the [Deploying a Registry Docs](https://docs.docker.com/registry/deploying/) for more info. Another option is [Docker Trusted Registry](https://docker-docs.netlify.app/ee/dtr/), it's great for enterprise applications, it sits behind your firewall, running on a swarm managed by Docker Universal Control Plane, and lets you securely store and manage your Docker images, mitigating the risk of breaches from the internet.

### Security Modules\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#security-modules "Direct Link to heading"\]\]

Docker supports several modules that let you write your own security profiles.

[AppArmor](https://www.apparmor.net/)is a kernel module that proactively protects the operating system and applications from external or internal threats, by enabling you to restrict programs' capabilities with per-program profiles. You can specify either a security policy by name, or by file path with the `apparmor` flag in docker run. Learn more about writing profiles, [here](https://gitlab.com/apparmor/apparmor/-/wikis/QuickProfileLanguage).

[Seccomp](https://en.wikipedia.org/wiki/Seccomp) (Secure Computing Mode) is a sandboxing facility in the Linux kernel that acts like a firewall for system calls (syscalls). It uses Berkeley Packet Filter (BPF) rules to filter syscalls and control how they are handled. These filters can significantly limit a containers access to the Docker Host's Linux kernel - especially for simple containers/applications. It requires a Linux-based Docker host, with secomp enabled, and you can check for this by running `docker info | grep seccomp`. A great resource for learning more about this is [DockerLabs](https://training.play-with-docker.com/security-seccomp/).

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Web Server Configuration\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#web-server-configuration "Direct Link to heading"\]\]

> _The following section only applies if you are not using Docker, and would like to use your own web server_

Dashy ships with a pre-configured Node.js server, in `server.js` which serves up the contents of the `./dist` directory on a given port. You can start the server by running `node server`. Note that the app must have been build (run `yarn build`), and you need [Node.js](https://nodejs.org) installed.

If you wish to run Dashy from a sub page (e.g. `example.com/dashy`), then just set the `BASE_URL` environmental variable to that page name (in this example, `/dashy`), before building the app, and the path to all assets will then resolve to the new path, instead of `./`.

However, since Dashy is just a static web application, it can be served with whatever server you like. The following section outlines how you can configure a web server.

Note, that if you choose not to use `server.js` to serve up the app, you will loose access to the following features:

- Loading page, while the app is building
- Writing config file to disk from the UI
- Website status indicators, and ping checks

Example Configs

- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#nginx\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#apache\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#caddy\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#firebase-hosting\]\]
- \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#cpanel\]\]

### NGINX\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#nginx-1 "Direct Link to heading"\]\]

Create a new file in `/etc/nginx/sites-enabled/dashy`

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">server {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    listen 8080;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    listen [::]:8080;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    root /var/www/dashy/html;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    index index.html;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    server_name your-domain.com www.your-domain.com;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    location / {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">        try_files $uri $uri/ =404;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    }</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">}</span></span>
```

Copy

To use HTML5 history mode (`appConfig.routingMode: history`), replace the inside of the location block with: `try_files $uri $uri/ /index.html;`.

Then upload the build contents of Dashy's dist directory to that location. For example: `scp -r ./dist/* [username]@[server_ip]:/var/www/dashy/html`

### Apache\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#apache-1 "Direct Link to heading"\]\]

Copy Dashy's dist folder to your apache server, `sudo cp -r ./dashy/dist /var/www/html/dashy`.

In your Apache config, `/etc/apche2/apache2.conf` add:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">&lt;Directory /var/www/html&gt;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    Options Indexes FollowSymLinks</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    AllowOverride All</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    Require all granted</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">&lt;/Directory&gt;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain" style="display: inline-block;">
</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">&lt;IfModule mod_rewrite.c&gt;</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  RewriteEngine On</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  RewriteBase /</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  RewriteRule ^index\.html$ - [L]</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  RewriteCond %{REQUEST_FILENAME} !-f</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  RewriteCond %{REQUEST_FILENAME} !-d</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  RewriteRule . /index.html [L]</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">&lt;/IfModule&gt;</span></span>
```

Copy

Add a `.htaccess` file within `/var/www/html/dashy/.htaccess`, and add:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">Options -MultiViews</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">RewriteEngine On</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">RewriteCond %{REQUEST_FILENAME} !-f</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">RewriteRule ^ index.html [QSA,L]</span></span>
```

Copy

Then restart Apache, with `sudo systemctl restart apache2`

### Caddy\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#caddy-1 "Direct Link to heading"\]\]

Caddy v2

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">try_files {path} /</span></span>
```

Copy

Caddy v1

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">rewrite {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  regexp .*</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  to {path} /</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">}</span></span>
```

Copy

### Firebase Hosting\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#firebase-hosting "Direct Link to heading"\]\]

Create a file names `firebase.json`, and populate it with something similar to:

```
<span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">{</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  "hosting": {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    "public": "dist",</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    "rewrites": [</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      {</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">        "source": "**",</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">        "destination": "/index.html"</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">      }</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">    ]</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">  }</span></span><span class="token-line" style="color: rgb(248, 248, 242);"><span class="token plain">}</span></span>
```

Copy

### cPanel\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#cpanel "Direct Link to heading"\]\]


1. Login to your WHM
2. Open 'Feature Manager' on the left sidebar
3. Under 'Manage feature list', click 'Edit'
4. Find 'Application manager' in the list, enable it and hit 'Save'
5. Log into your users cPanel account, and under 'Software' find 'Application Manager'
6. Click 'Register Application', fill in the form using the path that Dashy is located, and choose a domain, and hit 'Save'
7. The application should now show up in the list, click 'Ensure dependencies', and move the toggle switch to 'Enabled'
8. If you need to change the port, click 'Add environmental variable', give it the name 'PORT', choose a port number and press 'Save'.
9. Dashy should now be running at your selected path an on a given port

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Running a Modified Version of the App\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#running-a-modified-version-of-the-app "Direct Link to heading"\]\]

If you'd like to make any code changes to the app, and deploy your modified version, this section briefly explains how.

The first step is to fork the project on GitHub, and clone it to your local system. Next, install the dependencies (`yarn`), and start the development server (`yarn dev`) and visit `localhost:8080` in your browser. You can then make changes to the codebase, and see the live app update in real-time. Once you've finished, running `yarn build` will build the app for production, and output the assets into `./dist` which can then be deployed using a web server, CDN or the built-in Node server with `yarn start`. For more info on all of this, take a look at the [Developing Docs](https://dashy.to/docs/developing). To build your own Docker container from the modified app, see \[\[https://dashy.to/docs/management/#providing-assets#providing-assets#building-your-own-container\]\]

**\[\[https://dashy.to/docs/management/#providing-assets#providing-assets#top\]\]**


***

## Building Your Own Container\[\[<https://dashy.to/docs/management/>#providing-assets#\](<https://dashy.to/docs/management/>#providing-assets#building-your-own-container "Direct Link to heading"\]\]

Similar to above, you'll first need to fork and clone Dashy to your local system, and then install dependencies.

Then, either use Dashy's default `Dockerfile` as is, or modify it according to your needs.

To build and deploy locally, first build the app with: `docker build -t dashy .`, and then start the app with `docker run -p 8080:8080 --name my-dashboard dashy`. Or modify the `docker-compose.yml` file, replacing `image: lissy93/dashy` with `build: .` and run `docker compose up`.

Your container should now be running, and will appear in the list when you run `docker container ls –a`. If you'd like to enter the container, run `docker exec -it [container-id] /bin/ash`.

You may wish to upload your image to a container registry for easier access. Note that if you choose to do this on a public registry, please name your container something other than just 'dashy', to avoid confusion with the official image. You can push your build image, by running: `docker push ghcr.io/OWNER/IMAGE_NAME:latest`. You will first need to authenticate, this can be done by running `echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin`, where `CR_PAT` is an environmental variable containing a token generated from your GitHub account. For more info, see the [Container Registry Docs](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry).

> 
