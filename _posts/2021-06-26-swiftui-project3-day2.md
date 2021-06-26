---
layout: post
title: Swift UI Project 3, Day 2
categories: swift
date: 2021-06-26 8:36
author: alex
tags: swift swiftui
---

Another day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) today, basically applying the fundamentals we learned about yesterday.

My favorite part of it was that I got to use my new knowledge to make a custom Shape for .clipShape for a side project at work. I need a way to clip a view/color to a flag shape, and specifically to a [Swallowtail](https://en.wikipedia.org/wiki/Swallowtail_(flag) flag shape.

```swift
struct SwallowtailShape: Shape {
    var cutPercentage: CGFloat
    
    init(cutPercentage: CGFloat = 0.15) {
        self.cutPercentage = cutPercentage
    }
    
    func path(in rect: CGRect) -> Path {
        var path = Path()
        
        path.move(to: CGPoint(x: rect.minX, y: rect.minY))
        path.addLine(to: CGPoint(x: rect.maxX, y: rect.minY))
        path.addLine(to: CGPoint(x: rect.maxX - (rect.maxX * cutPercentage), y: rect.midY))
        path.addLine(to: CGPoint(x: rect.maxX, y: rect.maxY))
        path.addLine(to: CGPoint(x: rect.minX, y: rect.maxY))
        
        return path
    }
}

struct ContentView: View {
    var body: some View {
        Color.green
            .frame(width: 200, height: 100)
            .clipShape(SwallowtailShape())
        }
    }
}
```

And voila:

![Swallowtail Flag](/assets/swallowtail.png)
