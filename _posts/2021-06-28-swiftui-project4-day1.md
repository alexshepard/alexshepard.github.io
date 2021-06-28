---
layout: post
title: SwiftUI Project 4, Day 1
categories: swift
date: 2021-06-28 13:54
author: alex
tags: swift swiftui
---

Yay, more [100 Days of SwiftUI](https://www.hackingwithswift.com/100/swiftui) today!

I worked on some basic stuff: using Stepper to step through a range of numbers, and using DatePicker. I don't think I'll have much use for Stepper in an iNat app, but the SwfitUI DatePicker will be a signficant improvement to the third party component I'm using today.

We also created a simple tabular regressor model in Create ML. I sometimes train ML models for work using other tools, like Tensorflow. It was fun to see how easy it is to make a new model with Create ML. I asked for an Automatic algorithm and once trained, by opening the produced model I can see that it's a Feature Vectorizer -> GLM Regressor, so it looks like Create ML picked linear regression. I guess tomorrow we'll experiment with putting the model into the app and showing results. 

I'm not sure how applicable Create ML will ever be for iNaturalist - any models we make need to be available for web apps and Android as well as iOS. However, it could be a fun tool for prototyping different model types and experimenting with how to integrate ML techniques into mobile UI.