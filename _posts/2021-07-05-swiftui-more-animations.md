---
layout: post
title: More SwiftUI Animations
categories: swift
date: 2021-07-05 12:58
author: alex
tags: swift swiftui
---

Two small wins today: 
- I worked from a coffee shop for an hour, and
- I got another day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) done.

We covered more animation with SwiftUI today, and most of it was brand new to me. One hiccup I ran into: the SwiftUI preview canvas in Xcode beta 13 doesn't seem to render transition insertions correctly, but does render removal transitions correctly. Everything works OK in the simulator so maybe it's either a problem with the preview canvas or a beta bug? Either way, minor details.

I don't think I'll be using animations a ton at work, it's never seemed like a priority for us. We call that kind of stuff "sizzle." The implication being that it's not calories or sustenance, it's just shiny surface details. I don't entirely agree, but it makes sense for a research & science project.

However, when it comes to my tech art practice, movement and animation are gonna be very useful tools. Eventually I'd like to explore drawing (a la Processing or the Nature of Code) inside the SwiftUI [Canvas](https://developer.apple.com/documentation/swiftui/canvas). 

Another minor quirk: why is there a canvas in Xcode for previewing your SwiftUI layout _and_ a Canvas view type for immediate drawing in SwiftUI? Did they have to be named the same thing?
