---
layout: post
title: More Codable
categories: swift
date: 2021-07-21 9:49
author: alex
tags: swift swiftui generative-art
image: /assets/hello_shapes.png
---

Yay, another day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) wrapped up, and it's not even 10am. I'm going back into the office to do more work on iNat's new vision training server in a bit.

Today in 100 Days of SwiftUI we got back to projects. The section on adding Codable conformance for @Published properties, or adding custom Codable conformance to any class, was helpful. Cool to see how the CodingKey type works to make Codable work without keying everything by strings. The second section on using URLSession with Codable data was fun. I followed along with the basic implementation, then did my own using techniques that I've already learned while experimenting with the Xcode beta: using `.task { }` on a view to do async work, then moving all my network code into an async fetch function to avoid callback hell, and finally using a Result type to return either `.success(myData)` or `.failure(myError)` from the data fetch function. Very fun.

I also started on chapter two of [Generative Design](http://www.generative-gestaltung.de/2/) in SwiftUI and started exploring shapes. Until now, all of our explorations have been with rectangles and color.

![Hello shapes](/assets/hello_shapes.png)
