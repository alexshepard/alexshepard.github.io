---
layout: post
title: Swift UI Challenge Day
categories: swift
date: 2021-06-21 12:55
author: alex
tags: swift swiftui
---

Fun day today with [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui). The core challenge was very easy, a simpler version of the [PaperWeight app](https://apps.apple.com/app/apple-store/id1521170681?mt=8) I've been making with Nicholas.

However, after completing the basic challenge I decided to try using `Measurement` class to do my conversions. It worked fine, and made for a shorter and probably better solution. However, I tried using the iOS 15 `.formatted()` method on the converted measurement and while changes to the input length or input units flowed through the state system and triggered an update in the output, changes to the output format didn't seem to affect the computed output, even though the outputUnits was labelled with the `@State` property wrapper. Maybe the formatter is caching something?

Here's some code to illustrate:

```swift

struct ContentView: View {
    @State private var inputText = ""
    @State private var inputUnits = 0
    @State private var outputUnits = 4
    
    private var appleUnits = [
        UnitLength.meters,
        UnitLength.kilometers,
        UnitLength.feet,
        UnitLength.yards,
        UnitLength.miles,
    ]
    
    private var outputConverted: Measurement<UnitLength> {
        let numericInput: Double = Double(inputText) ?? 0.0
        
        let inputLength = Measurement(value: numericInput, unit: appleUnits[inputUnits])
        let outputLength = inputLength.converted(to: appleUnits[outputUnits])
        
        return outputLength
    }

    ...


    var body: some View {
        ...

        if #available(iOS 15.0, *) {
            Text("\(outputConverted.formatted())")
        }

    }
}
```

In this case, at least with Beta 1 of Xcode, changing the value in `inputUnits` triggers a full recalculation of the computed variable `outputConverted` and updates the UI. Changing the value in `outputUnits` does trigger a recalculation of `outputConverted` (I can see this with a breakpoint or print), but it doesn't update the UI.

Another day, another challenge with the beta apis for `FormatStyle`, I guess?
