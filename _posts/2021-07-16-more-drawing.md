---
layout: post
title: More Drawing
categories: swift
date: 2021-07-16 22:58
author: alex
tags: swift swiftui generative-art
image: /assets/self_portrait_brightness.jpeg
---

More [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) done today. I've used `CGAffineTransform` a little bit, but I'm still not really comfortable with 2d transforms (much less 3d). I guess if I wanna do a lot of drawing with code, I'll have to get comfortable with this.

I don't think I'll have much use for `ImagePaint` or even-odd fills (except for debugging), but `CGAffineTransform` and `.drawingGroup()` will definitely be a part of my toolkit going forward. I still have yet to watch the WWDC video on `Canvas` - [Add rich graphics to your SwiftUI app](https://developer.apple.com/videos/play/wwdc2021/10021/) - so I'll try to get to that over the weekend.

Meanwhile, I implemented another sketch in Swift/SwiftUI from the [Generative Design book](http://www.generative-gestaltung.de/2/) today, Color Palettes from Images. After re-implementing the p5js sketch in Swift, I kept going with the idea and wired up the camera to it, processing frames from the camera and then sorting pixels by hsb values. Here's a self-portrait, with sampled colors sorted by brightness.

![Self Portait, pixels sorted by brightness](/assets/self_portrait_brightness.jpeg)

I'm not sure my approach is totally optimal, I'm swapping between `UIImage`, `CGImage`, and `CIimage` formats and I worry that's moving the pixels from the GPU to the CPU and back again. Not really a problem for a one-off photo process, but working with video frames means I really need to pay attention to performance. I know next to nothing about Core Image but I wouldn't be surprised if there's a way with `CISampling` and `CIFilter` to sample the color from the pixels of an image into an array for sorting. More stuff to add to the list!