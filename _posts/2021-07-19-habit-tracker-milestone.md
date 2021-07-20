---
layout: post
title: Habit Tracker Milestone
categories: swift
date: 2021-07-19 23:39
author: alex
tags: swift swiftui generative-art
image: /assets/color_rules_transparency.png
---

Oh man, what a crazy day today. I got another day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) done, but the big change for me was having my first day back in the office since before COVID.

I had a lot of fun with the challenge today, but I struggled a little bit with incrementing the habit completion incrementer. Our `ObservableObject` activities is a class so it's mutable, and I can add and remove elements in its list of activities with no problem. But if each `Activity` is a struct, and that struct needs to have a modifiable element, then I guess we have to re-create the struct and re-insert it into the list? I definitely wasn't sure my implementation was ideal, but it works, so I guess I'm getting somewhere, right?

Meanwhile, I'm wrapping up my work on the Color chapter in the [Generative Design](http://www.generative-gestaltung.de/2/) book by re-implementing a few of the example sketches at the end of the chapter. Here's an example from my take on their Color Rules with Transparency sketch.

![Color rules with transparency](/assets/color_rules_transparency.png)