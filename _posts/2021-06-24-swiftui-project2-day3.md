---
layout: post
title: Swift UI Project 2, Day 3
categories: swift
date: 2021-06-24 10:58
author: alex
tags: swift swiftui
---

Iidn't sleep well last night - lingering pain from the dentist yesterday, and I also just don't really sleep anymore.

However, this morning I did get a early crack at [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui), wrapping up the GuessTheFlag tutorial and doing a few challenges. Nothing new to me in SwiftUI today.

One thing I'm noticing is that since everything is driven by state, when content needs to be shared between components (like say a function failing and triggering an alert while also supplying the text for an alert), that's done by adding the text to a state property on the main view. I struggle with that a little bit mentally - why does the main View need to always keep a string allocated just in case an alert message needs to be shown? What if the alert might only be shown once for every thousand users, isn't that just wasting memory? I suppose it's OK because it's cheap?