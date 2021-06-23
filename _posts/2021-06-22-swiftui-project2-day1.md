---
layout: post
title: Swift UI Project 2, Day 1
categories: swift
date: 2021-06-22 19::53
author: alex
tags: swift swiftui
---

Another fun day with [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui).

Some more basic views, but I'm already learning new stuff. I had no idea you could use colors and gradients directly as views! So cool. Also, it's pretty neat how `.edgesIgnoringSafeArea(.all)` modies one view or a group of views to extend beyond the safe area while the rest still honors the edges.

WWDC21 introduced some new stuff with buttons, and I spent the rest of my day 20 time re-watching the relevant portions of the [What's New in Swift UI](https://developer.apple.com/videos/play/wwdc2021/10018/) talk. I think I've already seen this talk twice, and I suppose I'll probably watch it again about 10 more times. It's good shit!

The bordered large button styles are perfect, who knows how many times I've made exactly these buttons out of a UITableViewCell. And the roles are cool. But how cool is `.confirmationDialog()` ?!? This is also something I've built by hand many times - Are you sure you want to delete that photo? Are you sure you want to remove that item from the project? Are you sure you want to blow up the moon? Well now it's simple and straightforward to build in declarative code, just like alerts and sheets:

```swift
struct ContentView: View {
    @State private var showDeleteMoonConfirmation = false
    var body: some View {
        VStack {
            if #available(iOS 15.0, *) {
                Button {
                    showDeleteMoonConfirmation = true
                } label: {
                    Text("Destroy the Moon").frame(maxWidth: 300)
                }
                .confirmationDialog("Are you sure?", isPresented: $showDeleteMoonConfirmation) {
                    Button("Do It", role: .destructive) {
                        print("KABOOOM")
                    }
                } message: {
                    Text("Deleting this will blow up the moon. Why? Who cares, it's not important to the plot.")
                }
                .buttonStyle(.bordered)
                .controlSize(.large)
                .controlProminence(.standard)
            }
        }
    }
}
```

So cool! 🥰