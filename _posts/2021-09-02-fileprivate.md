---
layout: post
title: fileprivate
categories: swift
date: 2021-09-02 12:27:08
author: alex
tags: swift swiftui generative-art
image: /assets/shapes_from_agents.png
---

Two more days of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) wrapped up. At work I've been cranking away at TF2, TFLite, and CoreML stuff. It's been nice to be able to really focus on vision stuff this week.

The most interesting thing for me the past few days has been the access modifiers, using `private` and `fileprivate` more on variables to enforce decoupling in my code. I definitely want to get into the habit of thinking about this stuff.

For today's image I'm working on a sketch from the [Generative Design book](http://www.generative-gestaltung.de/2/), using agents to deform a circle and drawing it iteratively as the user drags around the screen. Running into an issue with closed CatmulRom splines, so I have more work to do there.

![Shapes from agents](/assets/shapes_from_agents.png)
