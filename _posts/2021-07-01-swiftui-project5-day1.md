---
layout: post
title: SwiftUI Project 5, Day 1
categories: swift
date: 2021-07-01 11:30
author: alex
tags: swift swiftui
---

Some more bits of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) done today.

Nothing really new for me with `Lists` or using the app `Bundle`, but I hadn't used `UITextChecker` before, either in Swift or in Objective-C. Cool to see how to bridge from Swift strings to Objective-C strings.

More fun was experimenting with the iOS 15 beta's `.refreshable` modifier to see how much work a `List` has to do to re-examine the state when it has many, many items.  Feeding a `List` a `@State` array of 10,000 strings produces a body that simply takes a second to rebuild if the backing array changes. I initially thought the delay was caused by shuffling the array, because SwiftUI has seemed so fast and also it's structs man so it's magic! But while SwiftUI looks like magic, it can't break the laws of algorithmic complexity. If you ask it to do a ton of work, like comparing 10,000 strings to each other or building 10,000 list elements (even out of structs), there is a bit of work to be done there, and it may take a second.
