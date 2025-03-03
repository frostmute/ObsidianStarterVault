---
created: 2024-09-16
source: https://blog.dnsimple.com/2015/02/top-dns-servers/
category:
  - "[[Clippings]]"
cssclasses:
  - obsidian-banner
  - page-grid
  - pen-white
  - dashboard
poster: "![poster](../03%20-%20MEDIA%20&%20FILES/3e575006ee82218301e8b011184894f3_MD5.png)"
tags:
  - clippings
feature: "![[../03 - MEDIA & FILES/3e575006ee82218301e8b011184894f3_MD5.png]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/3e575006ee82218301e8b011184894f3_MD5.png)


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
url: https://blog.dnsimple.com/2015/02/top-dns-servers/
title: "The Top DNS Servers And What They Offer - DNSimple Blog"
description: "There are a lot of DNS Servers out there. We're looking at some of the top ones here and comparing their features and why some are chosen"
host: blog.dnsimple.com
image: https://blog.dnsimple.com/assets/images/illustrations/top-dns-servers.png
```

***
The Domain Name System is a core part of the Internet. There are many processes running in the background while you're doing something as simple as catching up on a blog like this one. One of the most important processes in simple web browsing is performed mostly by DNS servers, yet many developers have never learned much more than the name of one (or maybe two) DNS servers. Let's change that today.

## DNS as a part of the Internet

The domain name system, or simply DNS, may not be something you think of everyday. However, DNS is an essential piece of what makes the internet usable. When DNS is working properly, it's enough to type out a domain name into the URL bar in order to open a website, but if it weren't for DNS, we'd have to type in the IP address associated with that website in order to open it.

## The different DNS servers today

There are many different implementations of the DNS system today. Each DNS server represents a different implementation of characteristics, such as the interface, platform support, packaging and additional features.

### BIND

[BIND](https://www.isc.org/downloads/bind/) was designed in the early 1980 at the University of California Berkeley. Written by four students, BIND was and still is continually upgraded and is often considered the standard conventional DNS server. BIND is capable of serving as an authoritative name server as well as a recursor and supports many advanced DNS features such as DNSSEC, TSIG transfers, IPv6 networking. It can be managed via the command line or [with a web interface](http://www.debianhelp.co.uk/bindweb.htm). Even though it is mostly used on Unix-like operating systems, BIND is completely cross-platform today.

### PowerDNS

[PowerDNS](https://www.powerdns.com/) was created in the late 1990s in the Netherlands and quickly became one of the top providers of DNS software and services. The server itself is written in C++ and has a strong community of contributors. PowerDNS is just as full-featured as BIND, but is managed exclusively via a CLI. Many choose to deploy PowerDNS as it is a stable and robust DNS server while also being backed by strong community and commercial support.

### Unbound

Initially written in Java in 2006, [Unbound](https://unbound.net/) was rewritten in C by NLnet Labs as high-performance DNS server software in 2007. The strong points of Unbound are its modular components with modern features. Unbound is a recursive DNS resolver and so is not capable of acting as an authoritative name server, but modules are available for DNSSEC and an integrated client resolver API. Unbound was originally created for Unix-like operating systems, but has since been ported to Windows as well.

### Dnsmasq

[Dnsmasq](http://www.thekelleys.org.uk/dnsmasq/doc.html) was first released in 2001 under the GPL. As free software, Dnsmasq is a part of many Linux distributions today. Dnsmasq is mainly a DNS forwarder and a DHCP server managed via the command line. This software is lightweight and considered especially easy to configure. Dnsmasq is recommended for small networks on all operating systems with the exception of Windows.

### Erl-DNS

[Erl-DNS](https://github.com/dnsimple/erldns) is a full-fledged name server written in Erlang. It provides very fast query responses (30-65 *µs*/response) and can be used as an authoritative name server with several storage techniques for zone data. Erl-DNS lends itself nicely to being extended via Erlang's module system and is also quite fault tolerant due to Erlang's "let it crash" philosophy.

## Choosing a DNS server

At this point, you may feel that you're a bit overwhelmed. In fact, if I were to tell you to go out and start running your own DNS infrastructure using the information I've given here, I wouldn't be doing you any favors. Running your own DNS server is easy, running your own DNS infrastructure that performs well, is stable and resilient is not so easy.

![Running resilient DNS servers isn't easy](../03%20-%20MEDIA%20&%20FILES/f06746f5437069c879178196fb8837a4_MD5.jpg)

That said, there's good news! You don't have to run your own servers if you've got [a great managed DNS provider](https://dnsimple.com/). Not only can you register or [transfer domains](https://blog.dnsimple.com/2014/10/how-to-transfer-domains-without-downtime/), set up services like Google Apps and [purchase SSL certificates](https://support.dnsimple.com/articles/getting-started-ssl-certificates) from the comfort of your domain management page with us, but you'll also have the comfort of knowing that someone who knows how DNS can bite you is running your DNS servers.

## What we use

At DNSimple, we use a combination of technologies throughout our entire stack. Our nameservers are no exception. Presently we are running both Erl-DNS for our authoritative name servers, while also running PowerDNS for its excellent secondary DNS support. Both allow us to run a PostgreSQL database for zone data and we have proprietary methods for making zone updates available as soon as possible. Additionally, we are able to run Erl-DNS across a total of 40 nodes in 5 different global points of presence in an Anycast network. Additionally we are using other technologies which provide even more distributed points of presence and further variegated technologies to help with our mitigation against DDoS attacks.

We hope to provide easy to use, fast, and stable DNS service and our name server technology is just one of the ways we do that. If you haven't yet, [give us a try](https://dnsimple.com/pricing). We provide a 30-day free trial and are always willing to [help out with any questions you may have](https://dnsimple.com/contact).

Share on [Twitter](http://twitter.com/share?text=The%20Top%20DNS%20Servers%20And%20What%20They%20Offer&url=https://blog.dnsimple.com/2015/02/top-dns-servers/ "Tweet this post") and [Facebook](https://www.facebook.com/sharer/sharer.php?u=https://blog.dnsimple.com/2015/02/top-dns-servers/ "Share on Facebook")


#### Joseph Caudle

Teacher of people and computers. Fond of subtle distinctions.
> 