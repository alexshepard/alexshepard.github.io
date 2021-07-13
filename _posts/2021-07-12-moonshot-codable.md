---
layout: post
title: More Work with Codable
categories: swift
date: 2021-07-11 15:55
author: alex
tags: swift swiftui generative-art
---

Yay, another easy day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui)! I'm on day 40, that seems like a lot of days.

Only one thing was really new to me technically: using a `DateFormatter` to make a custom `.dateDecodingStrategy` for `JSONDecoder` is kinda cool, for those times when you can't just use the `.iso8601` strategy.

```swift
let decoder = JSONDecoder()
let formatter = DateFormatter()
formatter.dateFormat = "y-MM-dd"
decoder.dateDecodingStrategy = .formatted(formatter)
```

But more generally, the approach of stashing a bunch of JSON in the app and using an extension on `Bundle` to decode it is super helpful. I've been considering how best to add Preview Content to one of my apps for UI development and experimentation, when the content is typically delivered via an API. After today's session I have a pretty good idea of how I'll be doing it in my personal projects for now at least: stash copies of server responses into Preview Content and then use an extension on Bundle to quickly decode them for the preview.

Other things I learned yesterday? While doing [Generative Art](https://github.com/alexshepard/generativeart) experiments in Swift, after struggling with the lack of c-style for loops, I settled on using `stride()` to loop over a range with a step size:

```swift
for gridY in stride(from: 0, through: size.height, by: stepY) {
    for gridX in stride(from: 0, through: size.width, by: stepX) {
        // draw something in this grid square
    }
}
```

![Color Spectrum Grid](/assets/color_spectrum_grid.png)
