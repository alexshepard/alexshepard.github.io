---
layout: post
title: Swift UI Project 1, Day 3
categories: swift
date: 2021-06-20 22:20
author: alex
tags: swift swiftui
---

One more day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) done. I suppose this intro stuff will start getting boring, I'll have to come up with a better way of introducing my blog entries.

Today we reviewed the WeSplit app and did a few challenges. Everything was quite simple and straightforward. I did spend a bit of time trying to get the format stuff described at WWDC this year working with currency, but couldn't quite figure it out.

Apple showed some sample code like this:

```swift
var body: some View {
    ...

    TextField("New Person", value; $newAttendee, 
        format: .name(style: .medium))

    ...
}
```

and I suppose that works because newAttendee is a binding to an instance of `PersonNameComponents` with supports the FormatInput `.name`. And I see FormatStyle types in the docs for currencies, and they seem support Ints and Doubles, but when I try to supply `TextField` a value that's a binding to a Double, xcode complains. 

This is all new stuff and even the updates to [SwiftUI By Example](https://www.hackingwithswift.com/articles/195/learn-swiftui-with-swiftui-by-example_) for the new material from WWDC21 don't cover the new formatting in `TextField` so I guess I'll have to keep experimenting and looking at the beta docs this week.