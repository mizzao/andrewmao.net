---
id: 34
title: 'Sony Vaio Z website crashes Firefox &#038; Chromium in 64-bit Gentoo'
date: 2010-03-26T16:54:25+00:00
author: mizzao
layout: post
guid: http://www.mizzao.tk/?p=34
permalink: /2010/03/sony-vaio-z-website-crashes-firefox-chromium-in-64-bit-gentoo
categories:
  - Internet
tags:
  - Bugs
  - Internet
---
I was recently looking for a new laptop to buy and the Sony Vaio Z caught my eye. Its specs are quite amazing, and great for power users, especially the 1080p screen in a 13.3 inch size. However, I had a bit of trouble going to the <a href="http://www.sonystyle.com/webapp/wcs/stores/servlet/CategoryDisplay?catalogId=10551&storeId=10151&langId=-1&categoryId=8198552921644570897" target="_blank">product website</a> on my Linux desktop.

The first time I opened the link in Firefox, my system started paging after a few seconds, then froze completely. I couldn&#8217;t even kill GDM or log in from the Ctrl-Alt-F1 terminal. I thought that this must be a Firefox bug, so I reset the system and opened the page in Chrome.

Lo and behold, it crashed again. I had a chance to open up top before the system became completely unresponsive and saw that it was using almost 4GB of RAM, and growing. Killing the process disabled output to my monitors, so I had to ssh in and force a reboot.

This is a very mysterious problem, since the site doesn&#8217;t even use Flash, which I thought was mostly responsible for bugs and memory leaks like this. I wonder if the [OS hackers that couldn&#8217;t break Chrome](http://www.i4u.com/article32342.html) have been bested by the Sony website&#8230; I ended up having to open the page in my Windows XP VM.

For anyone trying to replicate the problem, I&#8217;m running 64-bit Gentoo and Firefox/Chrome are both compiled with emerge.