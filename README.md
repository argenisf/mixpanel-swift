<p align="center">
  <img src="https://github.com/mixpanel/mixpanel-swift-private/blob/assets/mixpanelswift.png?raw=true" alt="Mixpanel Swift Library" height="200"/>
</p>


[![Build Status](https://travis-ci.com/mixpanel/mixpanel-swift-private.svg?token=u1ndsoExx9snqasuDUsC&branch=master)](https://travis-ci.org/mixpanel/mixpanel-swift-private)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/mixpanel/mixpanel-swift-private.svg)](http://isitmaintained.com/project/mixpanel/mixpanel-swift-private "Average time to resolve an issue")
[![Percentage of issues still open](http://isitmaintained.com/badge/open/mixpanel/mixpanel-swift-private.svg)](http://isitmaintained.com/project/mixpanel/mixpanel-swift-private "Percentage of issues still open")
[![CocoaPods Version](http://img.shields.io/cocoapods/v/Mixpanel.svg?style=flat)](https://mixpanel.com)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![Apache License](http://img.shields.io/cocoapods/l/Mixpanel.svg?style=flat)](https://mixpanel.com)

# Introduction

Welcome to the official Mixpanel Swift Library

The Mixpanel Swift library for iOS is an open source project, and we'd love to see your contributions! 
We'd also love for you to come and work with us! Check out **[Jobs](http://boards.greenhouse.io/mixpanel/jobs/25226#.U_4JXEhORKU)** for details.

If you are using Objective-C, we recommend using our **[Objective-C Library](https://github.com/mixpanel/mixpanel-iphone)**

## Current supported features

* Tracking API
* Mixpanel People API
* Swift2.3 and latest [Swift3](https://github.com/mixpanel/mixpanel-swift-private/tree/swift3)
* [Full Documentation](https://mixpanel.github.io/mixpanel-swift-private/)

# Installation

## CocoaPods

Mixpanel supports `CocoaPods` for easy installation.
To Install, see our **[swift integration guide »](https://mixpanel.com/help/reference/swift)**

`pod 'Mixpanel-swift'`

(For this private repo please add this to the top of your pods file for integration):
`source 'git@github.com:mixpanel/PrivatePodSpecs.git'`

## Carthage

Mixpanel also supports `Carthage` to package your dependencies as a framework. Include the following dependency in your Cartfile:

`github "mixpanel/mixpanel-swift"`

(For this private repo please use this for integration):
`git "git@github.com:mixpanel/mixpanel-swift-private.git" "v1.0.3"`


Check out the **[Carthage docs »](https://github.com/Carthage/Carthage#if-youre-building-for-ios-tvos-or-watchos)** for more info. 

## Manual Installation

To help users stay up to date with the latests version of our iOS SDK, we always recommend integrating our SDK via CocoaPods, which simplifies version updates and dependency management. However, there are cases where users can't use CocoaPods. Not to worry, just follow these manual installation steps and you'll be all set.

### Step 1: Add as a Submodule

Add Mixpanel as a submodule to your local git repo like so:

```
git submodule add git@github.com:mixpanel/mixpanel-swift-private.git
```

Now the Mixpanel project and its files should be in your project folder! 

### Step 2: Drag Mixpanel to your project

Drag the Mixpanel.xcodeproj inside your sample project under the main sample project file:

![alt text](http://images.mxpnl.com/docs/2016-07-19%2023:34:02.724663-Screen%20Shot%202016-07-19%20at%204.33.34%20PM.png)

### Step 3: Embed the framework

Select your app .xcodeproj file. Under "General", add the Mixpanel framework as an embedded binary:

![alt text](http://images.mxpnl.com/docs/2016-07-19%2023:31:29.237158-add_framework.png)

### Step 4: Integrate!

Import Mixpanel into AppDelegate.swift, and initialize Mixpanel within `application:didFinishLaunchingWithOptions:`
![alt text](http://images.mxpnl.com/docs/2016-07-19%2023:27:03.724972-Screen%20Shot%202016-07-18%20at%207.16.51%20PM.png)

```
func application(_ application: UIApplication,
                 didFinishLaunchingWithOptions launchOptions: [NSObject: AnyObject]?) -> Bool {
    Mixpanel.initialize(token: "MIXPANEL_TOKEN")
}
```

# Initializing and Usage

By calling:
```
let mixpanel = Mixpanel.initialize(token: "MIXPANEL_TOKEN")
```

You initialize your mixpanel instance with the token provided to you on mixpanel.com.
To interact with the instance and start tracking, you can either use the mixpanel instance given when initializing:
```
mixpanel.track(event: "Tracked Event!")
```
or you can directly fetch the instance and use it from the Mixpanel object:
```
Mixpanel.mainInstance().track(event: "Tracked Event!")
```

## Start tracking

You're done! You've successfully integrated the Mixpanel SDK into your app. To stay up to speed on important SDK releases and updates, star or watch our repository on [Github](https://github.com/mixpanel/mixpanel-swift-private).

Have any questions? Reach out to [support@mixpanel.com](mailto:support@mixpanel.com) to speak to someone smart, quickly.
