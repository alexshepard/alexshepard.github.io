---
layout: post
title: Core Image, plus Core Data & Codable
categories: swift
date: 2021-08-05 12:56:17
author: alex
tags: swift swiftui generative-art
image: /assets/darkening_circles.png
---

Another day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) on the books. The UIViewControllerRepresentable stuff I'd done and seen before, but using Core Image filters was new to me. I feel like there's some wizardry to Core Image that'd help with my art stuff, but the learning curve is pretty steep. Kinda like it'll probably pay off to learn how to program shaders as I continue on this generative art journey. Added to the list.

I spent most of the day grinding on my iNat SwiftUI prototype, tackling serialization and infinite scrolling. I was able to use an example from [Donny Wals](https://www.donnywals.com)' book [Practical Core Data](https://www.donnywals.com/books/) as a starting point to understand how think about combining Core Data and Codable into the same model class. Then I just had to get it to work the way I wanted to, not as a syncing background data importer job, but as an lightweight async/await extension on URLSession to fetch lots of JSON records from an API and automatically save them. It feels kinda awkward to be basically re-creating RestKit after all these years. 🥵 

Another sketch from the [Generative Design book](http://www.generative-gestaltung.de/2/) today, with colors from a Marin landscape photo I took last week.

![Darkening Circles](/assets/darkening_circles.png)
