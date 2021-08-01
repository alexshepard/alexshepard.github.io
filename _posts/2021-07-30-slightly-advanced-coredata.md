---
layout: post
title: Slightly Advanced Core Data
categories: swift
date: 2021-07-31 12:22:20
author: alex
tags: swift swiftui generative-art
image: /assets/line_modules.png
---

I got some work done on [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) yesterday (the 30th) but I didn't do a generative art sketch or write this blog post until today (the 31st). Continued stomach issues, combined with visiting family, managed to derail me.

Lots of new stuff in Core Data & SwiftUI for me yesterday, including a nice pattern for dynamically filtering a `@FetchRequest` with a custom SwiftUI view.

I tried doing today's Generative Art sketch in a slightly different way. I've been frustrated that I haven't figured out good ways to abstract the drawing commands I want to execute inside the `Canvas` object. In particular, I haven't figured out how to just pass it a `Shape` file and say "stroke this `Shape` in this `CGRect` using these line characteristics." It seems possible with `context.resolveSymbol()` but I haven't gotten that to work. So today I tried making an extension on `Path` to create a custom initializer, a la `Path(ellipseIn:)` that would just draw my custom `Path` inside any rect I wanted. It mostly worked, but abstracting the `Path` away like that also makes it harder to change lineweight or stroke color on just a part of that `Path`, since that's done further out in the `Canvas` context. So I guess tradeoffs.

```swift
extension Path {
    init(radiatingLinesIn rect: CGRect, lineCountPerSide: Int = 10) {
        assert(lineCountPerSide >= 1, "line count per side must be at least 1")
        
        self.init()
        let origin = CGPoint(x: rect.midX, y: rect.midY)
        
        for side in 0..<4 {
            var x2: CGFloat = .zero
            var y2: CGFloat = .zero
            
            for i in 0..<lineCountPerSide {
                if side == 0 {
                    // top side - left to right
                    x2 = rect.minX + (rect.size.width / CGFloat(lineCountPerSide)) * CGFloat(i)
                    y2 = rect.minY
                } else if side == 1 {
                    // left side, bottom to top
                    x2 = rect.minX
                    y2 = rect.maxY - (rect.size.height / CGFloat(lineCountPerSide)) * CGFloat(i)
                } else if side == 2 {
                    // right side, top to bottom
                    x2 = rect.maxX
                    y2 = rect.minY + (rect.size.height / CGFloat(lineCountPerSide)) * CGFloat(i)
                } else if side == 3 {
                    // bottom side, right to left
                    x2 = rect.maxX - (rect.size.width / CGFloat(lineCountPerSide)) * CGFloat(i)
                    y2 = rect.maxY
                }
                let end = CGPoint(x: x2, y: y2)
                move(to: origin)
                addLine(to: end)
            }
        }
    }
}
```

![Line modules](/assets/line_modules.png)
