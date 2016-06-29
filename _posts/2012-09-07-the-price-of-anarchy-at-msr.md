---
id: 166
title: The Price of Anarchy at MSR
date: 2012-09-07T16:52:58+00:00
author: mizzao
layout: post
guid: http://www.andrewmao.net/?p=166
permalink: /2012/09/the-price-of-anarchy-at-msr
categories:
  - Research
---
I&#8217;m not an algorithmic game theory researcher by any means, but I&#8217;ve heard the term &#8220;Price of Anarchy&#8221; tossed around a few times, most memorably by [Costis Daskalakis](http://people.csail.mit.edu/costis/) in his 6.896 course when I was a student: &#8220;<it> has been beaten to death.&#8221; I took this to mean that most of the interesting research in the area had already been done, and that perhaps the number of practical applications weren&#8217;t that numerous.

Well, I&#8217;m getting a real, live taste of the price of anarchy this summer, at MSR Redmond where I am an intern. No, the company is not going broke, nor is [the research division getting cut](http://www.pcmag.com/article2/0,2817,2403915,00.asp). This is a much less weighty situation involving the distribution and allocation of MATLAB licenses. You see, at a company like Microsoft, licensed software such as MATLAB is exactly that &#8211; everyone must have a license to use it. There is a central server with a fixed amount of licenses that can be allocated to users at a given time, and when the allocation is filled, someone has to close their MATLAB instance before someone else can open one.

I have no doubt that there are enough licenses available to go around for everyone who actually needs to use MATLAB to be able to use it. In this perfect world, users would close their instance and free up their license when they are done. However, most users who try to run MATLAB during the day get an error that all the licenses are taken and they must try again later. Why is this? Well, it turns out that a good number of users, including the vast majority of the interns, have adopted the strategy of keeping MATLAB open all the time in case they need to use it later, never freeing up their license unless their computer shuts down and loses power, and generally compounding the problem even more. The typical water cooler talk often involves some complaining about how no MATLAB licenses are available.

From a game-theoretic point of view, this is an evolutionary game, where there are two strategies that can be played by the population: a) Open the program only when needed and close it when done, or b) keep the program running all the time in case there are no licenses available when you need it. Let&#8217;s call a) Cooperate and b) Defect. There are two equilibria that are stable; 1) when everyone plays Cooperate, because there are enough licenses to go around, and there is no added incentive to defect; and 2) when everyone plays Defect, because Cooperating means you will pretty much never get to use the program. The 1) Cooperate equilibrium is efficient, since everyone who has a license is actually using it productively. However, equilibrium 1) is unstable, since once a few users start defecting, there ends up being a license shortage and then everyone must switch to the Defect strategy to have any chance of using MATLAB. As expected, the efficiency of the Defect equilibrium is horrible because a significant fraction of licenses are allocated to users who aren&#8217;t actually using them and are working on something else.

Occasionally, there is talk that we should just buy more licenses, and perhaps that would solve the problem. But I think that may not be necessary. I&#8217;m hoping to hear some useful suggestions from Price of Anarchy or evolutionary game theory researchers about how to change the incentives here to move things into the more efficient equilibrium. Here&#8217;s a chance to apply your research to a practical problem!