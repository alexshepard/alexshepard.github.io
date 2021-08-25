---
layout: post
title: Project Meishi and Catmull-Rom splines
categories: swift
date: 2021-08-25 10:19:10
author: alex
tags: swift swiftui generative-art
image: /assets/draw_moire.png
---

One more day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) finished. Well, I finished the SwiftUI bits yesterday. I didn't end up writing this today because I decided to try to figure out how to implement interpoloating splines in Swift. Yesterday I got discouraged and gave up after a frustrating try at it, but this morning, with fresh eyes, I was able to get it working.

Our SwiftUI project yesterday was basically a business card app. I called it [Meishi](https://en.wikipedia.org/wiki/Business_card#Japan), after the Japanese word for calling or visiting card. It was a bunch of work but nothing too challenging, and it definitely felt nice to be able to finish an app like that in just over an hour, even adding Core Data support. It reminded me of an interview challenge I did a few years back, where I floundered because I decided to implement it with Core Data, but then I couldn't remember everything necessary to get a Core Data stack working within the interview time window. The new Persistence controller in the Core Data template in the Xcode beta certainly helps, but it's also way easier to connect fetch requests to UI in SwiftUI. Not to mention, I've done three or four Core Data projects in the past few weeks so I'm feeling pretty confident.

For today's image, I started with yet another moire sketch, from the [Generative Design book](http://www.generative-gestaltung.de/2/). However, the sketch in the book uses a P5.js method called [curveVertex](https://p5js.org/reference/#/p5/curveVertex) that uses [continuous interpolating splines](https://en.wikipedia.org/wiki/Centripetal_Catmull–Rom_spline) under the hood. I wanted to do the same thing in Swift, but iOS has no built-in method for doing this. It took me a day or so, but I eventually got something working. I even managed to get it to work using the Accelerate framework, which is a first for me. This image uses an implementation _before_ I got interpolating splines working, because I like the way the moire looks with more jitter.

![Drawing with Moire](/assets/draw_moire.png)
