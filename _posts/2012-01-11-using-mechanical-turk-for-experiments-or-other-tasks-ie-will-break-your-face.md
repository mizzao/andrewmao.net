---
id: 147
title: Using Mechanical Turk for experiments or other tasks? IE will break your face.
date: 2012-01-11T15:20:25+00:00
author: mizzao
layout: post
guid: http://www.andrewmao.net/?p=147
permalink: /2012/01/using-mechanical-turk-for-experiments-or-other-tasks-ie-will-break-your-face
categories:
  - Uncategorized
---
Like many other research experimenters and crowdsourcing businesses, I use Amazon Mechanical Turk to get some real human input on my tasks. For a project I&#8217;ve been doing recently, I wanted to make the information input as easy as possible, so I wrote an application using lots of Javascript, with jQuery and CometD libraries, in modern standards-compliant HTML.

Everything worked great in Firefox and Chrome. However, the first time I ran the task, I neglected to test the task in IE. I was puzzled as I watched it run, since many users accepted the task and returned it after some amount of reloading. Since the task itself was pretty straightforward, I figured that there must be some problem with the browser mechanics.

As I began testing in IE, I realized I&#8217;d just discovered the eccentric world of web compatibility. Prior to IE9, there was no way to debug Javascript in IE. However, IE9 has started to catch up to other browsers by offering a debugger and tools for examining the DOM. I also discovered that since previous versions of IE were so bad, IE9 had the option to render pages with the engine used for each of them, since sites would break under modern standards.

<p style="text-align: center;">
  IE9 is a pretty huge improvement from previous versions of IE. However, there are some things that Microsoft still refuses to get right. The behavior that was breaking my application was how IE9 renders an IFrame in an existing page: it forces the IFrame to render with the same engine as the parent page. Since Mechanical Turk hasn&#8217;t updated its site to use <!doctype html> (HTML5 standards) yet, my entire task was being rendered in &#8220;Quirks Mode&#8221; &#8211; aka, what was used in IE 5.5. My standards-compliant, modern CSS-and-Javascript application was completely broken.
</p><figure id="attachment_149" style="width: 610px" class="wp-caption aligncenter">

[<img class=" wp-image-149 " title="IE9's one-engine rendering system" src="http://www.andrewmao.net/blog/wp-content/uploads/2012/01/crap.png" alt="" width="610" height="107" />](http://www.andrewmao.net/blog/wp-content/uploads/2012/01/crap.png)<figcaption class="wp-caption-text">Great! Thanks, IE!</figcaption></figure> 

What&#8217;s more, there was no way to override this behavior with <meta> tags or changes to the doctype. Microsoft has even stated that this is the standard behavior and it won&#8217;t be changed. I was surprised, since IE has so many override options given how different previous versions have been. I ended up fixing my application for IE by replacing all unsupported functions with custom Javascript or jQuery functions, and using the IE Javascript shim for CSS. What a nightmare! It&#8217;s really too bad that so many people use IE, but collecting experimental data with only Firefox/Chrome users might bias one&#8217;s data <img src="http://www.andrewmao.net/blog/wp-includes/images/smilies/simple-smile.png" alt=":)" class="wp-smiley" style="height: 1em; max-height: 1em;" />

For more information on this behavior, you can see the following post.

<http://css-tricks.com/ie-iframe-quirksmode/>