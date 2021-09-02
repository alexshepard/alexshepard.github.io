---
layout: post
title: Another Catchup Day
categories: swift
date: 2021-08-30 12:46:28
author: alex
tags: swift swiftui generative-art
image: /assets/intelligent_agents.png
---

Some catchup on the blog today. I've been mostly keeping up with [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) but haven't been writing. Just feeling a little too overwhelmed with everything. So I'm not going to write much here today, just that I'm done with day 81 and looking forward to wrapping the whole thing up in a few weeks.

For today's image, another sketch from the [Generative Design book](http://www.generative-gestaltung.de/2/). The big challenge here was how to determine if the actively drawing line intersects with a previously drawn line. In the book they load the pixels and see if the canvas has been draw to at that point, but in Swift I had to do some trig to calculate the distance from a point to a line segment.

![Intelligent agents](/assets/intelligent_agents.png)
