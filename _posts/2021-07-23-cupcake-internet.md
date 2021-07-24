---
layout: post
title: Cupcake Internet
categories: swift
date: 2021-07-23 21:47:23
author: alex
tags: swift swiftui generative-art
image: /assets/alignment_grid_symbols.jpg
---

A bit more [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) done today, but the big news is that I learned a ton about `Canvas`! I'll get to that in a minute. Nothing really new with the CupcakeCorner project, we added `Codable` support to our Order object and did some basic network requests. I hadn't used [REQ\|RES](https://reqres.in/) before so that was cool to learn about, I'd always used [requestbin](https://requestbin.com). I can see advantages for each.

But on to the exciting stuff. I started looking at some of the SVG examples in chapter 2 of the [Generative Design](http://www.generative-gestaltung.de/2/) book and quickly realized that the approaches I'd been using in SwiftUI weren't going to cut it. So I went back and finally watched the WWDC video called [Add rich graphics to your SwiftUI app](https://developer.apple.com/videos/play/wwdc2021/10021/) and the last 10 minutes or so are a great introduction to using `Canvas`. I learned so much that I'm already putting into practice. For example, instead of creating a `Timer` and then attaching it to our view with `.onReceive(timer) { }`, I can just wrap my `Canvas` in a `TimelineView` and then get the time interval out of the timeline parameter to key animations of the drawing operations on my canvas. I also learned about drawing images quickly with `context.resolve` and blend modes and even went further and explored translation and rotation. And how cool is it that you can make an inner copy of a context and then apply translations or rotations on the inner copy, then do some drawing with the inner copy, then when you go back to using the outer copy, the transformations aren't applied anymore. Very much like `pushMatrix()` and `popMatrix()` in Processing. Oh, what a lovely day.

Here's a basic animation that I did with SwiftUI using `TimelineView`, `Canvas`, and "circle.hexagongrid.fill."

![Animated alignment in a grid with symbols](/assets/alignment_grid_symbols.mov)
