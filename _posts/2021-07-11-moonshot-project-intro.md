---
layout: post
title: Moonshot Project Intro
categories: swift
date: 2021-07-11 15:55
author: alex
tags: swift swiftui generative-art
---

Man, it's ups and downs all week. I'm mentally doing well but struggling physically today. Happily, I've stuck with [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) and gotten another day done.

I'd only just started exploring `GeometryReader` in my generative art experiments recently, so it was nice to see it introduced in 100 Days of SwiftUI today. I guess we have to wait a few weeks to cover it in detail. SwiftUI's `ScrollView` was new-ish to me as of last week. Only yesterday I started using it in my iNat SwiftUI prototype, so it was nice to get a proper introduction. Meanwhile, the other two main topics covered, `NavigationLink` and hierarchical `Codable` data, were not really new at all for me.

I have a bit of an intro for my [Generative Art](https://github.com/alexshepard/generativeart) work. Off and on, over the last year, I've been teaching myself to make digitial art and doing digital drawing using some popular tech art frameworks like Processing and P5.js. I briefly tried doing it with Swift a few years ago, but making art out of UIKit view hierarchies was limiting (especially on an iPad in Swift Playgrounds). Happily, SwiftUI comes to the rescue. The new `Canvas` view type in the beta version of SwiftUI is great for doing dynamic drawing, and it can take hints about the screen size if wrapped in a `GeometryReader`. After that, all that I needed to do was draw into the `Canvas` to make a digital drawing, and I was even able to animate my drawing using a `Timer` that was attached to the View hierarchy using the `.onReceive()` modifier. Next steps will be to go back and re-implement some of my favorite Processing and P5.js sketches in Swift using this little framework I've spun up.

