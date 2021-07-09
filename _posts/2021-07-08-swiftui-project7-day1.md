---
layout: post
title: SwiftUI Project 7, Day 1
categories: swift
date: 2021-07-09 01:45
author: alex
tags: swift swiftui
---

Late night tonight. I didn't get a session of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) between everything else that was going on, so I started it near midnight.

I've used @ObservableObject before, but I'm not sure I totally understood what made it different from a @State struct, despite the obvious difference implied in the name (one's a reference type, one's a value type). It was good to go over it in a little more detail.

A few other interesting things that were new to me:
- I hadn't come across closing a sheet with `presentationMode` before,
- I hadn't used UserDefaults in SwiftUI before, and
- I've used Codable a lot with network JSON but I hadn't used it with UserDefaults.

All together a nice list of bits and bobs, a few of whihch I'll be migrating into my SwiftUI rewrite of iNat shortly. That's coming along nicely, by the way, I got login working with Apple's AuthenticationServices which I hadn't used before, and got started on a camera / new observation flow.
