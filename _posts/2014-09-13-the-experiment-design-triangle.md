---
id: 257
title: The Experiment Design Triangle
date: 2014-09-13T11:14:24+00:00
author: mizzao
layout: post
guid: http://www.andrewmao.net/?p=257
permalink: /2014/09/the-experiment-design-triangle
categories:
  - Experiments
  - Mechanical Turk
  - Research
---
Perhaps you&#8217;ve heard of the [project management triangle](http://en.wikipedia.org/wiki/Project_management_triangle): it&#8217;s often been encapsulated as &#8220;fast, good, or cheap: pick two&#8221;; because it&#8217;s been invariably impossible to satisfy all three in executing projects.

In designing web-based behavioral experiments, I&#8217;ve found that there is a similar triangle of three desirable properties that are very difficult to satisfy simultaneously:

  * **Large sample size** &#8211; desirable to increase experiment power
  * **Large number of simultaneous arrivals** &#8211; whether for synchronous experiments or to minimize time-of-day effects across treatments (see also [this post](http://www.andrewmao.net/2014/08/what-can-you-do-with-100-turkers-online-all-at-the-same-time "What can you do with 100 Turkers online all at the same time?"))
  * **Unique participants** &#8211; i.e. those who haven&#8217;t seen the study before

When running large experiments that are synchronous or require extensive randomization, and that are constrained to unique participants, one will naturally run into the sample size ceiling. It is feasible to recruit about 1500 to 2000 active workers on MTurk on any given week, but fewer and fewer of them are available at the same time as you schedule your experiments.

Alternatively, this means that if you can design your experiments to be less sensitive to repeat participation, it&#8217;s possible to have a lot of people participate and also gather a lot of data. I&#8217;ve done this for previous experiments, but it can be challenging to ensure that the design is answering the right question, and that participants aren&#8217;t being primed from past experiences.

Finally, the vast majority of online studies that are done don&#8217;t require simultaneous arrivals because either they are for single users or they are not scheduled consistently at the same time of day. Without this constraint, it&#8217;s possible to have many unique participants with a sample size of a couple thousand or more, but one should be careful that region and time-of-day effects are being controlled for.