---
layout: post
title: Swift UI Project 3, Day 1
categories: swift
date: 2021-06-25 9:53
author: alex
tags: swift swiftui
---

More [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) today, learning some fundamentals for how SwiftUI actually does things under the hood.

Mostly review for me, but it was cool to go over custom view composition again since that's something I haven't done in a while. One thing new for me, I didn't realize how easy it was to make custom modifiers, so much fun!

```swift
struct WeddingModifier: ViewModifier {
    func body(content: Content) -> some View {
        content
            .font(.custom("Zapfino", size: 24))
    }
}

extension Text {
    func weddingText() -> some View {
        self.modifier(WeddingModifier())
    }
}

struct MyView: View {
    var body: some View {
        Text("Hello, World")
            .weddingText()
    }
}
```
