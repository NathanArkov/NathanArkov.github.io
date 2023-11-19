---
layout: post
title:  "How to make your own media server at home with Jellyfin and the Arr stack"
date:   2023-11-19
featured_image: 2023-11-19-my-homelab-setup/blog-thumbnail.png
tags: [Networking, Homelab]
---

I have been interested in home servers and self hosting for almost a year now, and today I figured I would show you the state of my lab as of November 2023. 

<!--more-->

# Introduction

I've always liked self-hosting as well as networking and hardware. So a homelab was kind of a must-have for me. It's far from perfect, far from efficient, but hey, I'm still on the learning curve and try to upgrade it day by day by making modifications that could simplify processes or just making everything work nicely.

# Networking

{% include image_full.html imageurl="/images/posts/2023-11-19-my-homelab-setup/network.jpg" title="My networking setup" caption="My networking setup" %}

## Router 1

I got an old **Netgear PROSAFE FVS336G v2** for less then 10 bucks online and got it in my mail 4 days later. The main goal buying this router was to replace my now *second* router to get Gigabit Ethernet in my room. As of today I'm still living at my parent's house, and a single CAT6 ethernet cable runs through the walls into my room, so I added a router to have all of my stuff in my own network and have more control over it.

{% include image_full.html imageurl="/images/posts/2023-11-19-my-homelab-setup/router1.jpg" title="Netgear PROSAFE FVS336G v2" caption="Netgear PROSAFE FVS336G v2" %}

This is a dual WAN Firewall with SSL and IPSec VPN from before 2017. It has 4 Gigabit LAN ethernet ports and 2 Gigabit WAN ethernet ports, and that's pretty much it. I'm still not using it to it's full potential though and only use it as a simple router. In the future I'd like to experiment more with the firewall, as well as site to site VPNs.

## Router 2

This router is a **Netgear N300 WNR2200**. I got it years ago for 5€ and used it as my first very own router. The gret thing with this router is that it can handle wifi, which is great for my room that has some IoT needs (mainly my phone, but also Nintendo Switch, Amazon Fire TV Stick etc). 

{% include image_full.html imageurl="/images/posts/2023-11-19-my-homelab-setup/router2.jpg" title="Netgear N300 WNR2200" caption="Netgear N300 WNR2200" %}

I had to buy another router once my needs expended as it only have 5 FastEthernet RJ45 ports, and I got a (*allegedly*) 2Gbps fiber connection to my house. This is why now it is only used as a Wifi access point for guests and IoT.

## Switch

At the moment, I only use a small TP Link 5 ports Gigabit unmanaged switch to connect everything to the routers.

# Main server

The machine I use as a server right now is my old gaming desktop. It is kind of old and I decided to keep it when I upgraded to a newer one. So, one day, I wanted to do something better out of this pile of hardware collecting dust in a corner of my room, so I installed **Proxmox** on it !

{% include image_full.html imageurl="/images/posts/2023-11-19-my-homelab-setup/tour.jpg" title="Main server" caption="Main server" %}

It currently runs on :
- an Intel core i5 3570k CPU @ 3.40GHz (Quad core)
- 16Gb of DDR3 RAM
- One 1Tb HDD and One 2Tb HDD
- an NVIDIA GTX660 (not in use right now)

While decent as a gaming PC, I find it more efficient as a server. It runs at around 100W with load and around 70 to 80W on idle, and contains all of my VMs.

Currently, I run a TrueNAS Core VM, a media server VM (Jellyfin + qBittorrent + Arr Stack) and a small LXC Container for Homarr !

I have to say when under load, the CPU has a bit of struggle to keep up with all it's cores used, but still manages to work - *most of the time*. One of the HDD has some bad sectors so I'll need to figure that up in the following days as all of my services currently doesn't work anymore.


# Rack mounted stuff

One day while in class, a friend of mine and I were looking at listings for old used servers and other IT parts, when we found this : a listing for multiple servers and computers for only 40€ ! Our first thought was that it was a scam and it either wasn't the real price, or nothing would work. After calling the guy selling it, we learned that it was in fact not a dream nor a scam, just a network engineer in the process of moving houses that needed to clear space.

Being two dumbs IT student we jumped in the car and got there the same night, where we discovered a SUN Microsystems server, a Fujitsu, 3 IBMs, a Dell, multiple old (*really* old) computers and two Overland tape libraries.

Long story short, I kept some computers, the **DELL PowerEdge 2850** and the **FUJITSU PRIMERGY RX300 S3**. 

{% include image_full.html imageurl="/images/posts/2023-11-19-my-homelab-setup/rack-1.jpg" title="Bunch of rack mounted stuff" caption="Bunch of rack mounted stuff" %}

I got lucky and both where full and working, only missing redondant PSUs. The only thing I had to check was on the Fujitsu, as the power button was broken. So I quickly got the PCB, desoldered the old button and soldered a new one - *works like a charm*.

I also bought for a bit less than 40€ online a **Cisco ASA 5510** firewall and a **Netgear GS724Tv4** switch. I haven't got time to play with the switch, and I tried messing with the Cisco firewall but couldn't get the software to work yet. Projects for another day.

All of this is currently sitting on the floor in my room as I'm testing things with it and doesn't own a rack yet (I plan to build one). Also, I've checked and each server draws twice as much current as my current server, for less performance, so I'm not sure they'll be plugged in 24/7 in the near future.

# Future plans

In the future I plan to :

- Expend my homelab : buy more stuff that I need / enjoy testing with. For example maybe a Cisco Catalyst switch so I can train to get the CCNA Certification?
- Try pfsense/opnsense: I recently bought **4 HP T620** for 50€ and plan to add a second ethernet port on one to use as a pfsense router, while I'll keep the 3 other ones to do projects with.
- Fix my current installation and customize it. I'd really want a Bitwarden instance as well as a NAS to store my files / backups. But for that I'd also need to put my lab on the internet and that's something I'm not currently skilled enough to do securely.

In a nutshell, I hope I'll be able to learn more, experiment more, and have more fun with IT.