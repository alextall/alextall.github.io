---
layout: post
title:  "Automating Maintenance"
date:   2015-08-23 19:52:24 -0000
categories:
---

I wasted a Saturday afternoon tinkering with my .bash_profile and automating some of the regular maintenance I run on my Mac Mini Server, so I thought I would share it in the off chance it could save someone time.

First up, we have a sript that will check for all HFS volumes and check the filesystem for errors. I have a Drobo 5D hooked up to my server and various other drives can be connected from time to time, so I thought it would be nice to have all drives scanned. If any errors are found, they will not be automatically repaired. Instead a file will be place on the desktop stating that the drive in question needs repair.

<script data-preserve-html-node="true" src="https://gist.github.com/alextall/e051d54a9abd04ae56d3.js"></script>

Next, I set up a launchd agent to automatically run this script every Saturday at midnight.

<script data-preserve-html-node="true" src="https://gist.github.com/alextall/3491d783ecf977726c9a.js"></script>

As a side note, because this is running on my server I have also set Hazel to push a notification to my MacBook if that file ever appears on the desktop of the server.

I use <a href="http://brew.sh">Homebrew</a> to install and update some of the software/services I run on my server. Beacuse I don't depend on this software for anything critical, I would rather updates be installed automatically. So I set up another launchd agent that will kick this off every week.

<script data-preserve-html-node="true" src="https://gist.github.com/alextall/2ced356f29112ad6b022.js"></script>
