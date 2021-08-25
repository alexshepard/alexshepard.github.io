---
layout: post
title: Meishi with MapKit
categories: swift
date: 2021-08-25 15:22:52
author: alex
tags: swift swiftui generative-art
image: /assets/clot.png
---

Another day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) done. We had to integrate MapKit into the visiting card app that I named Meishi yesterday. I think the only tricky bit was handling optional locations in Core Data. 0, 0 is a [legal location](https://en.wikipedia.org/wiki/Null_Island) in the world, so the default value for a double in Core Data of zero won't work. Instead, I set a custom default value of -180 for latitude and longitude in the model, which is what's in the latitude & longitude values in [kCLLocationCoordinate2DInvalid](https://developer.apple.com/documentation/corelocation/kcllocationcoordinate2dinvalid) so it's easy to check against at runtime.

Today's image is a riff on the Dumb Agents sketch in the [Generative Design book](http://www.generative-gestaltung.de/2/). I changed the color & density to feel like a blood clot, which is a thought that's always in the back of my mind.

![Clot, dumb agents](/assets/clot.png)
