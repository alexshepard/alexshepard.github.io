---
layout: post
title: SwiftUI Project 5, Day 3
categories: swift
date: 2021-07-03 12:27
author: alex
tags: swift swiftui
---

One more [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) project in the books today.

The most interesting bit of the challenges for Project 5 was calculating the score - for me it seemed like a case for using swift's `reduce` function. I don't do a lot of functional programming (any, really) so I don't remember the syntax and I also don't really remember the mental model for how the functions work. But after a quick look at the docs for `Array.reduce` I came up with:

```swift
private var score: Int {
    return usedWords.reduce(0, { x, y in
        x + y.count
    })
}
```

where usedWords is an array of Strings.

I also immediately wanted to add a persistent high scores function to this app. I'm sure we'll be getting to data persistence with Core Data or I suppose wrapping UserDefaults eventually, so I'll just made a non-persistent version for now, with an `@EnvironmentObject` that gets created by our game's `ContentView` and stuffed into the environment with the `.environmentObject()` modifier. Then all we have to do is keep it up to date as the user plays the game and read it out of the environment in our high score list if the user presents that sheet. Fun!

