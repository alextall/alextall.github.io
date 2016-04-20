---
layout: post
title:  "Automating the Transcode"
date:   2015-02-06 04:40:24 -0000
categories:
---

I'll spare you the story of me suffering through a shoddy old rip of a DVD, but suffice it to say that about 3 weeks ago I decided I needed to re-rip my movie collection for better quality. Thankfully <a href="http://twitter.com/donmelton">Don Melton</a> has already done all of the hard work with his <a href="https://github.com/donmelton/video-transcoding-scripts">video transcoding scripts</a>.

SIDE NOTE: At about this point, it should be noted that the ripping/encoding of video can take a long time on even the fastest computers. I have a Mac Mini Server that largely sits idle, so that computer has been dedicated to helping with this task.

I knew that I had a lot of movies and TV shows to re-encode, so I wanted to automate as much of the process as possible. I set up <a href="http://www.makemkv.com">MakeMKV</a> to automatically rip any DVD/BluRay disc into Matroksa (.mkv) files using the simple script below.<script src="https://gist.github.com/alextall/995d19500909682e0afb.js"></script>This sets up a directory full of uncompressed videos in a flexible, if not very compatible, format. If that works for you, great! You're done. But I like to keep my media in iTunes for easy streaming to my Apple TVs, so I set up Hazel to watch the directory in the script above.

  <img src="http://static1.squarespace.com/static/521e80f7e4b0fe1b7d940134/521e831ce4b0bf248fe90ee7/54d4436ee4b0b97e05e8227c/1423197039379//img.png" alt=""/>




  <img src="http://static1.squarespace.com/static/521e80f7e4b0fe1b7d940134/521e831ce4b0bf248fe90ee7/54d44336e4b0bc3abee41904/1423196983079/Screen+Shot+2015-02-05+at+9.48.00+PM.png.00+PM.png?format=original" alt=""/>


The resulting action from Hazel is an embedded script. I took some liberties with the batch management script Don provides and added some automatic crop detection (using Don's crop detection script) as well as automatically including all audio streams and subtitles. NOTE: Crop detection and is not used in the transcode currently, and neither are subtitles added. Last but not least, we do some cleanup. I like to keep the source files for later re-encoding as well as the log files if troubleshooting becomes necessary, so these files need to go somewhere.<script src="https://gist.github.com/alextall/570c870fb12d8bef2681.js"></script>This has been a work in progress for a few weeks, but given the amount of time I have spent on this, I thought someone else might benefit from it. Click the source link below to get to the Github repository.
