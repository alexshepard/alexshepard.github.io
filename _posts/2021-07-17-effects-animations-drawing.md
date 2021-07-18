---
layout: post
title: AnimatableData and Spirographs
categories: swift
date: 2021-07-17 19:15
author: alex
tags: swift swiftui generative-art
image: /assets/spiro_stride.png
---

A bit more [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) finished today. 

We covered `AnimatableData` today, which has already made it across to my [Generative Art](https://github.com/alexshepard/generativeart) explorations. In particular, the AnimatedAcrossShapes sketch uses a stack of `AnimatablePair` structs to stash four animatable `CGFloat`s on a shape. The spirograph was awesome. I had fun extending the presented material by experimenting with the amount you stride across theta by, to make other geometric shapes.

![Spiro Stride By](/assets/spiro_stride.png)
![Spiro Stride Two](/assets/spiro_stride_two.png)
![Spiro Stride Gradient](/assets/spiro_stride_gradient.png)