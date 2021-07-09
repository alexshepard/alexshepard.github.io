---
layout: post
title: SwiftUI Project 7, Day 1
categories: swift
date: 2021-07-09 01:45
author: alex
tags: swift swiftui
---

Late night tonight. I didn't get to a session of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) with everything else that was going on, so I started it near midnight.

I'd used the `@ObservableObject` property wrapper before, but I'm not sure I totally understood what made it different from `@State`, despite the obvious difference implied in the name (one wraps reference types, one wraps value types). It was good to go over why you'd use `@ObservableObject` in a little more detail.

A few other things that were new to me:
- I hadn't come across closing a sheet with `@Environment(\.presentationMode)`,
- I hadn't used UserDefaults in SwiftUI, and
- I've used Codable a fair bit with network JSON but I hadn't used it with UserDefaults.

All together a nice list of bits and bobs, a few of whihch I'll be migrating into my SwiftUI rewrite of iNat straight away. That's coming along nicely, by the way, I got login working with Apple's AuthenticationServices which I hadn't used before, and got started on a camera / new observation flow.
