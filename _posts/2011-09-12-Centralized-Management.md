---
layout: post
title:  "Centralized Management Begins"
date:   2011-09-12 01:10:15 -0000
categories:
---

As a part of my ever-growing need to know all things tech-related, I have been exploring centralized device management... in the home.

First, a brief description of my home network. I have two Macs, Jen's iMac, and my MacBook Pro. We each have an iPad, iPhone, and a slew of iPods. There is also an Apple TV connected to the TV. We use a Time Capsule to provide DHCP/NAT and as our sole wireless access point. The wireless network is hidden, runs on dual frequencies, and has a guest network that is also encrypted. My machine also hosts a slew of virtual machines, most of which are connected using a NAT built into my virtual server of choice.

Jen always has trouble remembering the pass code to the network (partially by design, as I am using part of the MAC address of an old modem that I no long use), and this was my first reason for testing the waters of central device management. Now that I have spent more time learning (read: playing) with Profile Manager in Lion Server, I realize there is a lot more than I was ever aware of. I have created a single profile that I distributed to all of our devices, iOS and OS X alike, which automatically adds our wireless network(s) and the associated pass code and sets pass code requirements for the devices themselves.

This is really only a small part of where I am looking to be, because both Jen and I are looking at new computers. Her because the iMac is getting a little long in the tooth, me, because my usage is changing and the 15in MBP is more than I need. When we do get our new machines, I want to hit the ground running. While Time Machine can do wonders, we're both looking at different usage scenarios afterwards, and it just seems right to start fresh without all the old cruft we've built up.

That's why the first machine we get will be a Mac Mini Server. Why so much hardware on a home server, you ask? The quad-core goodness will really hep out when I'm using qadministrator to delve out tasks from my MacBook Air, as well as the hard drive pace should be plenty (at least for now) for us to store network home folders. As our storage needs grow, I'll be able to add fast storage easily as more Thunderbolt devices come to market. Once we get the Mac Mini, I can restore a Time Machine backup to it from the Lion Server VM I'm using now, getting us up and running in no time. We'll also be hosting NetBoot services in order to self-triage any issues we may encounter as well as host NetRestore images in case we ever need to NAR (nuke and repave) as it was once explained to me in training. (Being the nerds we are, taking our own machines to the Genius Bar just seems weak). I'll also be setting up web services (hopefully I'll be able to find a way to self-host by then, and you'll be reading this from my own private server) and VPN so we can use the web securely, even when an encrypted network isn't available.
