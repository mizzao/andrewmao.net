---
id: 199
title: A Meteor has hit TurkServer!
date: 2013-06-18T10:37:59+00:00
author: mizzao
layout: post
guid: http://www.andrewmao.net/?p=199
permalink: /2013/06/a-meteor-has-hit-turkserver
categories:
  - Internet
  - Research
---
Over the last few weeks, I&#8217;ve been playing around with building web apps in the [Meteor](http://www.meteor.com/) framework &#8211; specifically, some online experiments that I&#8217;ve been imagining that require constant real-time interaction between large numbers of participants. It seems that the excitement about Meteor really started about a year ago in mid-2012, and it has gained a large following and significant userbase (almost 9000 stars on GitHub as of today), which is an imperative for a web framework to have staying power in the flavor-of-the-day framework scene.

Meteor&#8217;s development paradigm is significantly different from almost all other web frameworks, which focus on the front-end or back-end. (I&#8217;ve been using [Spine](http://spinejs.com/) as a client-side MVC framework recently.)  It is a full-stack web framework, where the server-side code runs on Node.js and the client-side runs in the browser. Code is mostly written declaratively rather than imperatively &#8211; instead of saying _how_ you want to do something, you just write _what_ you want to do. Most importantly, the core of Meteor is a distributed data framework (which the declarative style hooks into) that greatly simplifies synchronizing state between multiple clients and a server. This is another level of abstraction over AJAX &#8211; instead of worrying about passing messages or calling remote procedures, you can just specify the data that needs to be shared and it will be updated, in real time, transparently. The result? From my experience, it&#8217;s an order of magnitude reduction in the amount of code that needs to be written for a real-time or collaborative app. As one article put it, [Meteor has made MVC obsolete](http://newcome.wordpress.com/2012/04/14/the-future-of-web-development-isnt-mvc-its-mvm/). When leveraging front-end frameworks such as Twitter&#8217;s Bootstrap that integrate well with Meteor, the amount of custom CSS that needs to be written is greatly reduced as well.

Here are some great examples of apps in Meteor. Be sure to use them from multiple browsers simultaneously:

  * <span style="line-height: 14px;"><a href="http://realtime-redlines.meteor.com/">http://realtime-redlines.meteor.com</a> &#8211; draw on and annotate a map<br /> </span>
  * [http://hangwithme.meteor.com](http://hangwithme.meteor.com/) &#8211; multiplayer hangman!
  * [http://cocodojo.meteor.com](http://cocodojo.meteor.com/) &#8211; CoCoDoJo, a collaborative IDE
  * [http://madewith.meteor.com](http://madewith.meteor.com/) &#8211; Keeps track of the most interesting apps made with meteor, itself a meteor app.
  * [http://www.discovermeteor.com](http://www.discovermeteor.com/) &#8211; The Meteor book, which I&#8217;ve been reading &#8211; highly recommended, and itself a Meteor app

Now consider how much code these apps took to write. Back in the day, you might expect around 10,000 lines. However, the first two (redlines and hangman) are less than a couple hundred lines of JS excluding some visual components. That&#8217;s quite insane considering what these apps allow for.

What&#8217;s the punch for academic experimenters? Well, if you&#8217;ve been doing online experiments or followed the TurkServer project at all, you&#8217;ve probably realized while reading this post that Meteor probably does a lot of things that you (or I) want to do, except a lot better. A lot of the custom programming in TurkServer was to allow for real-time interaction between participants, but that&#8217;s cake now with Meteor. Additionally, while TurkServer already reduces the coding load greatly compared to rolling your own app, it&#8217;s still a decent amount of work, and there aren&#8217;t many examples to use.

The natural next step came to me as quite an inspiration: TurkServer would be better suited as an add-on for Meteor, taking any Meteor app and running it on MTurk. There are tons of example apps floating around upon that are very similar to experiments that people have in mind, and being able to contribute full-stack code makes components such as a lobby (waiting room), chat, and other components much easier to drop-in. I&#8217;ve realized that this approach can fix quite a few of the existing annoyances with TurkServer as well.

The future of online experiments is coming, and the next generation of web technologies is a great force multiplier for getting things done!

* * *

**UPDATE**: See [What can you do with 100 Turkers online all at the same time?](http://www.andrewmao.net/2014/08/what-can-you-do-with-100-turkers-online-all-at-the-same-time "What can you do with 100 Turkers online all at the same time?") for how the original ideas in this post have been developed.

The current version of this software is at <https://github.com/HarvardEconCS/turkserver-meteor>. I haven&#8217;t begun widely promoting it yet, but I&#8217;ll document and release to the public after my current experimental research projects are written up.