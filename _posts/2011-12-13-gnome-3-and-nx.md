---
id: 110
title: Gnome 3 and NX
date: 2011-12-13T18:46:32+00:00
author: mizzao
layout: post
guid: http://www.andrewmao.net/?p=110
permalink: /2011/12/gnome-3-and-nx
categories:
  - Linux
tags:
  - Gnome
  - NX
---
I&#8217;ve been using NX for a while. For those of you who don&#8217;t know what it is, it&#8217;s a highly customized X server for fast remote desktop connections. Clients are supported from Windows, OS X, and Linux, and sessions can be disconnected and reconnected from any client. The best part is that it doesn&#8217;t lag at all. I can write code without noticing any hiccups, and I&#8217;ve even used it from a Bolt Bus. Can you say that about RDP or VNC? NX has been a mega productivity tool for me and I&#8217;ve proselytized it to many fellow graduate students as well.

Recently, Gnome 3 has been released and is slowly stabilizing into Linux releases. With its compositing and massive UI improvements, Linux is finally exiting the Dark Ages of user interface and getting features comparable to Windows 7 and OS X. Gnome 3 is very different from Gnome 2, and requires some familiarization with keyboard shortcuts to be productive. Once you&#8217;ve learned them, you won&#8217;t regret it, though.

The problem with NX is that its custom X server doesn&#8217;t support many of the latest X features, especially compositing. However, I wanted to have both the power of the full Gnome 3 UI when at work and the flexibility of NX when I needed to access my work from anywhere else. I finally made the jump to Gnome 3 on my main work computer, and found that it has a fallback mode that works under NX, similar to the old Gnome 2 UI. However, the layout is super ugly.

If you want to go this route as well, you&#8217;ll want to download some Gnome 2 Themes and put them in your `~/.themes/` directory, making your NX session prettier more usable. Otherwise, the experience is pretty much the same as Gnome 2.

NX 4 is supposed to support compositing though, so look forward to that! Even so, you might not want to use it to maximize performance over slower connections.

If anyone else has experience using both NX and Gnome 3, feel free to pitch in!