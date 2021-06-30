---
layout: post
title: SwiftUI Project 4, Day 3
categories: swift
date: 2021-06-30 1:20
author: alex
tags: swift swiftui
---


Another day, another bit of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) done.

If yesterday was simple, today was simpler. The challenges amounted to:
- changing some VStacks to Sections, something I'd already settled on yesterday since I didn't like how the VStacks were looking,
- swapping a Stepper with a Picker, which just required rethinking the binding a bit since with a Stepper the binding is to the user's chosen value, but in a Picker driven by a Range, the binding is to the index of the chosen value inside the Range, so there's off by one potential, and finally
- changing the UI to always show the recommended bedtime instead of having a "calculate" button - which was the best challenge, since the UI actually feels natural and automatic now.

I also did some Create ML stuff yesterday, including training a classification model on some of iNat's data on my little M1 Macbook Air. When I tried to load in my sample training set with ~500k images, I ran into a problem where training shut down with no feedback other than "Unexpected error" which wasn't terribly helpful. In the end I made two changes and got training going:
1. switched to a different, smaller dataset of just 50k images (which could point to a data quality issue in the larger dataset, perhaps non-jpegs in the set, or could point to a dataset size problem), and
2. worked with my laptop open instead of closed (potentially avoiding overheating issues, since the M1 MBA has no fan). 

I guess as I have time today I'll try to figure out which of these caused the Unexpected error and try to work around it.

