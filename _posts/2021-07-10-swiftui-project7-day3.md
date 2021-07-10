---
layout: post
title: iExpense Project Wrap-up
categories: swift
date: 2021-07-10 14:00
author: alex
tags: swift swiftui
---

I'm feeling a little better today, jamming to [KEXP](https://www.kexp.org) and working on some [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui). 

The challenges today were fun, although two of them highlighted more general issues I'm having with SwiftUI:
- Adding text styling based on the amount was simple enough, but as far as I can tell, you need to use a ternary operator inside modifiers like `.foregroundColor()` or `.fontWeight()`, which means if you need to allow for multiple options, you need to use nested ternary operators, which gets messy and ugly as the number of options grows. Maybe there's a better way?
- Also, adding validation feedback to the amount field in our iExpense app led me down a rabbit hole of looking at all the initializers for `TextField()` - some require formatters, some require prompts, some require strings to be wrapped in `Text()` views while others do not, etc. The variety of different initializers for views in SwiftUI can get a little bewildering. They're not always easy to decode with help from the compiler, either. Using an invalid initializer for a View inside an `if #availabile()` block can cause the whole body to fail validation for generic reasons like `Return type of property 'body' requires that 'EmptyCommands' conform to 'View'`, whereas it would be helpful in that case to say `For this initializer you need to provide a formatter` or something. To be fair, some of this may be down to Xcode beta issues.

At any rate, still really enjoying myself with SwiftUI and the [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) project.