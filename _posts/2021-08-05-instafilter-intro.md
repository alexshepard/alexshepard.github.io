---
layout: post
title: Custom Bindings
categories: swift
date: 2021-08-05 12:56:17
author: alex
tags: swift swiftui generative-art
image: /assets/selfie_lines_color.png
---

First day back on [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) after a cracking [Hacking with Swift: Live!](https://www.hackingwithswift.com/live) conference. I was inspired by the talks but also by my fellow attendees!

Today we covered some basics for how `@State` actually wraps a value, and peeked under the hood at how to wrap the `@State` struct with a custom binding to inject behavior a la `didSet` or `didGet`. Paul also introduced ActionSheets, which have since been deprecated in the beta in favor of confirmation dialogs. The only thing I don't like about `.confirmationDialog()` right now is that I'm likely to forget that `titleVisibility` defaults to `.hidden` on my iPhone.

```swift
.confirmationDialog("Change background", isPresented: $showingActionSheet, titleVisibility: .visible) {
    Button("Mint") { self.backgroundColor = .mint }
    Button("Purple") { self.backgroundColor = .purple }
}
```

Here's a modification to my luminosity sketch from earlier, adding color to the mix.

![Selfie with Lines, Color](/assets/selfie_lines_color.png)
