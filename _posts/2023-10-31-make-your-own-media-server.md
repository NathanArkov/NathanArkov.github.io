---
layout: post
title:  "How to make your own media server at home with Jellyfin and the Arr stack"
date:   2023-10-31
featured_image: grand-canyon.jpg
tags: [Travel, Blogging]
---

Have you ever wanted to free yourself from your multiple monthly subscription to Netflix, Amazon Prime Video, Disney+, etc ? **Self-hosting is the answer**. Today, I'm going to show you how you can build your own media server to download, manage and -most importantly- watch your favorite movies and show. For this, you will either need **a server** (an old computer will most likely do the trick) or **a virtual machine** running 24/7 (or everytime you want to watch something).

**DISCLAIMER** : To build your own media server, many alternatives exists. In this post, I'm going to show you how to install and configure *Jellyfin, Radarr, Sonarr, Lidarr, Readarr and qBittorrent* on a server, but keep in mind you could also do it using *Docker* or replace some software with other ones like Plex (Media Server) or Deluge (Torrent).

<!--more-->

# Requirements
As I said earlier, we're going to install our media server on a virtual machine (VM) / server. In my case, I'll be using a **Debian 12** VM hosted on my Proxmox VE home server.
I recommend using at least a 4 vCPUs VM (4 cores) and 8GB of RAM to be sure everything goes smoothly. 

The other thing you're gonna need is storage, **a lot of it**. Movies and TV Shows can quickly take a lot of space in your hard drive. So I advice you to use multiple big hard drives or a NAS to store your data. Also, if you can, remember to setup RAID so that you don't loose your content if one of your hard drives malfunction.

Finally, I strongly suggest you use a VPN in order to download content. You can find tutorials on the internet on how you can link up your VPN to qBittorrent.

# Installation

## Jellyfin installation

First of all, we're going to update the debian repositories using this command.
```bash
sudo apt update
```

Then, if you don't have it, you will need to install cURL
```bash
sudo apt install cURL
```

Thankfully, Jellyfin installation is pretty straight forward, the only command you will need to run is
```bash
curl https://repo.jellyfin.org/install-debuntu.sh | sudo bash
```

## qBittorrent installation

## Radarr, Sonarr, Lidarr, Readarr installation


# Conclusion