---
layout: post
title: Moonshot Project Challenges
categories: swift
date: 2021-07-14 22:16
author: alex
tags: swift swiftui
---

Another day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) finished. 

The challenges today were the most involved yet. Partly what's fun about the challenges is that they're becoming less about "remember how to do this thing, and then do it" and more about "which of several ways are you going to do this thing?" In particular, the fact that of almost all of our data model is now needed on every screen of the app leads me to the question: at what point does a data model just belong in the environment if it's passed everywhere? I don't really know, I'm not really current on SwiftUI best practices for things like what to use the environment for, and what not to. 

On the one hand it seems like the environment could easily just become a place to stuff global variables, which we all know is bad, right? On the other hand, passing the same data model into every constructor is gonna get old, especially if the view hierarchy looks like A -> B -> C and only A and C depend on model _Z_, then B needs to keep track of _Z_ just in case it has to pass it on to C.

Just something to get in mind, I guess. Onward!
