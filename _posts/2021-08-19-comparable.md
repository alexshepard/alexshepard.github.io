---
layout: post
title: Comparable
categories: swift
date: 2021-08-19 18:15:38
author: alex
tags: swift swiftui generative-art
image: /assets/moire_circle.png
---

Slowly getting back into the rhythym with [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) after a break. I tackled Day 71 yesterday where we add `Comparable` conformance to a `Codable` struct and downloaded some data from Wikipedia.

Unfortuately, I'm running into a bug where the simulator freezes every minute or two due to a breakpoint inside Apple's stuff, `_os_semaphore_dispose.cold.1`. The recommendation on the Apple developer forums is to rollback to Xcode Beta 4. I suppose I could upgrade my OS to the beta, since that's probably of why Apple didn't catch it before releasing Xcode Beta 5. Hardly the end of the world, it just makes app development kinda slow.

Here's a sketch straight out of the [Generative Design book](http://www.generative-gestaltung.de/2/), redone in SwiftUI. Moire from two overlapping sets of concentric circles.

![Moire Circles](/assets/moire_circle.png)
