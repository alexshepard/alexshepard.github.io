---
layout: post
title: Swift UI Project 1, Day 2
categories: swift
date: 2021-06-19 15:10
author: alex
tags: swift swiftui
---

Another day of [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) on the books. Today we built the WeSplit UI and wired everything up.

My only significant change to today's work was using a NumberFormatter to display the amount per person instead of using a c-style format string. I see that Apple added new formats to TextField in WWDC this year, but I'm not sure how that applies to output only Text views. I also added a header title to the result section since it's just kinda hanging out there without an explanation.