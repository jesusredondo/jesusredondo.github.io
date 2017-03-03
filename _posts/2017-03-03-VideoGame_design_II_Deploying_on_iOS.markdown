---
layout: post
title:  "Video Game Design II: DEPLOYING LIBGDX ON IOS"
date:   2017-03-03 17:20:00 +0100
categories: project
---

In this second entry I am going to review all the neccesary steps to build the default LibGDX base project. The example will be running on two different platforms: Desktop (which is pretty much straightforward if you follow the [wiki]( https://github.com/libgdx/libgdx/wiki) and iOS. Testing our project in our Apple phone devices… well, it can be a bit tricky, it is not hard, but you have to scrupulously follow some steps. 

If you want to try the same project on Android devices there is enough documentation in the LibGDX wiki.

It is true that this entry breaks a little bit the flow on the video games developing series, but this is so important that I think is well worth leaving everything written down before moving on.


### Prerequisites:


1. **IDE** → [IntelliJ IDEA]( https://www.jetbrains.com/idea)

2. **Hardware I am using** → Macbook Pro retina mid 2014 and iPhone 5c.

3. **Apple Developer Account (free version)** → In order to sign the app being created we need an Apple Developer Account. This account is free and will allow us to sign apps to be used in our devices, although we obviously can’t publish them in the App Store. If we also want do so, we mush adhere to the [Apple Developer Program]( https://developer.apple.com/programs/), which costs 100€ per year.



## Step 1: Download LibGDX framework and create a new project.

Go to the [LibGDX download page](https://libgdx.badlogicgames.com/download.html) and run the jar. We fill up the available options as follows:

<img alt="libgx-entry2-1" src="/images/gameDevelop/2/1.png" width="700">

As you can see we are only generating Desktop and iOS projects.

**BEWARE**: Before finishing, go to “Advanced” and tick “
