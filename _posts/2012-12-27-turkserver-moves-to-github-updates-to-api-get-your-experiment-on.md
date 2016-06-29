---
id: 174
title: 'TurkServer moves to GitHub, updates to API &#8211; Get your experiment on!'
date: 2012-12-27T02:59:47+00:00
author: mizzao
layout: post
guid: http://www.andrewmao.net/?p=174
permalink: /2012/12/turkserver-moves-to-github-updates-to-api-get-your-experiment-on
categories:
  - Uncategorized
---
Recently, I&#8217;ve been doing a lot of coding for TurkServer, revamping the API and making it easier to use. I&#8217;ve also <a href="https://github.com/HarvardEconCS/TurkServer" target="_blank">moved the project over to GitHub</a>, not only because Git is massively superior to SVN, but also because GitHub offers a unique social atmosphere for working on open-source software that is much better than the semi-closed model that SVN projects use. Others can fork a project, create some great updates, and send those back to the main project in the form of a pull request. It&#8217;s a great distributed way to work on open source!

I&#8217;ve started to document the API a little, as well as giving some additional technical instructions on coding with TurkServer. You can check out the progress on the <a href="https://github.com/HarvardEconCS/TurkServer/wiki" target="_blank">Turkserver wiki</a>. Although things are still not complete yet, there should be enough to get you started if you are interested in trying your next group experiment on MTurk &#8211; and you should be! I&#8217;m always open to specific requests to finish a section of the documentation that is particularly in demand.

I&#8217;m currently working on a new version of a GUI and bootstrapping code for running experiments, but the core API and infrastructure is all there &#8211; so please feel free to try coding up some simple experiment ideas and testing them out. You can use the client API to create simulated workers that pretend to be coming from MTurk and take some dumb actions in your experiment. Perhaps you want people to chat with each other, play a game with each other, trade money with each other&#8230;the possibilities are endless! You&#8217;ll be surprised at how little code you need to write to implement a real-time, group interaction experiment on MTurk.

However, one thing I&#8217;ve begun to understand a bit more recently is the importance of building a good user interface, for both social science and human computation experiments. If you look at experiments done over the last decade, the lack of usability of interfaces presented to participants was just horrible. However, we have great tools for dealing with that now, such as the interactivity from HTML5 technologies and single-page Javascript applications, which are perfect for making experiment interfaces. TurkServer provides a Javascript library so you can use it to hook up clients with such an interface, and I build almost all of my experiments in JS now. I prefer to use CoffeeScript and Spine &#8211; check out a <a href="http://stackoverflow.com/questions/9425368/spine-js-hem-server-hem-build-faq-for-windows/12595619#12595619" target="_blank">StackOverflow post I made recently</a> on this. Along with promoting TurkServer, I hope to promote great user interfaces &#8211; not only because they will get you better data, but because your participants will be much happier and interested in your experience!