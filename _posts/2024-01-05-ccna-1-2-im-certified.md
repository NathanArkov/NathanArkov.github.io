---
layout: post
title:  "CCNA 1 & CCNA 2 : I'm certified"
date:   2024-01-05
featured_image: 2023-11-24-ccna/blog-thumbnail.png
tags: [Networking, CCNA]
---

The Cisco Certified Network Associate (CCNA) certification is a widely recognized entry-level certification in the field of networking. It validates the skills and knowledge required to install, operate, and troubleshoot small to medium-sized enterprise networks.

Cisco CCNA 1 certification, specifically version 7, is the first module of the CCNA curriculum. It covers fundamental networking concepts, including network components, infrastructure, and basic network security principles. CCNA 1 focuses on building a solid foundation in networking, introducing learners to key concepts and skills that serve as a basis for more advanced topics in subsequent CCNA modules. In this article, I am gonna document my journey through this course.

<!--more-->

# Networking Today

## Network Components

This section of the course teaches us about the core of networking: what is an host, how can they communicate, and really just a bunch of vocabulary and basic things. We can especially define :

- **Host**: All computers connected and participating in a network are called hosts. This term refers to a device having a **IP address** *(Internet Protocol) to identify them on a network. 
- **Client**: Type of host having software to *request* and display informations obtained from a server.
- **Server**: Type of host having software allowing them to *provide* information to clients.
- **End Device**: Either the source or the destination of a message transmitted over a network. e.g. a smartphone, a desktop computer...
- **Intermediary Device**: They are used to connect end devices to a network. They can connect to multiple networks and use the destination end device address, in addition to informations about the network connections to determine the path the message will take through the network. e.g. a router, a switch, a firewall...

{% include image_full.html imageurl="/images/posts/2023-11-24-ccna/client-server-schema.png" title="Simple Client - Server connection through internet" caption="Simple Client - Server connection through internet" %}

We also learn that data is transported through a network by three major means : **Copper** where it is encoded as electrical pulses (cables), **Fiber-optic** where it is encoded as pulses of light in a glass tube, and **Wirelessly** where it is encoded as a modulation of frequencies of electromagnetic waves. We have to chose carefully which network media we will use for a network and ask us some questions :

- *What will be the distance traveled by the information ?*
- *In which information will the media be installed ?*
- *What is it costs ?*
- *How much data will be transported, and at which speed ?*

## Network Representations and Topology

When designing a network, we create **diagrams** following some conventions. In the world of Cisco, these are the main components of a networking diagram :

{% include image_full.html imageurl="/images/posts/2023-11-24-ccna/diagram-icons.png" title="Cisco Icons & Symbols" caption="Cisco Icons & Symbols" %}

**Topology diagrams** provide a visual representation of how the network is connected. We can distinguished to type of topology diagrams : **Physical** and **Logical**.

### Physical Topology Diagrams

{% include image_full.html imageurl="/images/posts/2023-11-24-ccna/physical-topology-diagram.PNG" title="Physical topology diagram example" caption="Physical topology diagram example" %}

This type of topology diagrams informs us about the **physical location** of devices in the installation. You can clearly see room numbers, shelf numbers...

### Logical Topology Diagrams

{% include image_full.html imageurl="/images/posts/2023-11-24-ccna/logical-topology-diagram.PNG" title="Logical topology diagram example" caption="Logical topology diagram example" %}

This type of topology diagram informs us about the **devices, ports and addressing** of the network. You can see what type of network media is used to connect devices and on which interface it is plugged in.

## Types of Networks

Two type of networks are most commonly used: **LANs** and **WANs**. A LAN is a small network connecting together a few hosts over a small geographic area. Whereas a WAN is used to connect many hosts in a large geographic area and is commonly managed by an ISP.

The Internet is a worlwide collection of interconnected networks (**internet**works). LANs connect together throughs WANs that connects together, creating millions of networks connected together on the internet.

An **Intranet** is a private collection of LANs and WANs belonging to an organization. It is usely designed to be only accessed by members or employees of this organization to permit secure communication. In some cases, individuals that doen't belong to the organization still need a safe access to the organization data, that's where an **Extranet** is used.

## Packet Tracer 1.5.5 LAB - Network Representation

This lab is pretty straight forward and mainly relies on observation. Opening the Cisco Packet Tracer file results in seeing three LANs connected to an internet cloud : The Home office, the Central and the Branch. Central and branch are also connected to an Intranet. We are asked to identify intermediary devices, end devices, and are asked a few questions about LANs and WANs in the lab. Some fairly simple questions are added as a "bonus" at the end like "*Add an end device to one of the LAN, how are you going to connect it ?*", the answer being connecting it to a switch, setting it's IP address to one available in the same *subnet* as other devices in this LAN, and setting the next router IP address as a gateway.


# Conclusion

This part of the course was fairly simple but still felt quite nice. It is always good to refresh your memory on the basic stuff you tend to forget over the time. I still have much more work to put in, but I'm excited as I think this is going to be a challenge for me.

I'm ready to face this challenge.