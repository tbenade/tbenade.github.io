---
layout: post
title:  "Getting Ionic and Android Studio up and running on OS X Mavericks"
excerpt: "The absolute noob guide to getting up and running with Ionic Framework"
date:   2014-07-18 12:47:01
tags: [Android Studio, AngularJS, Hybrid, Ionic, Ionic Framework, Mavericks, OSX]
comments: true

---

<img style="float:left; padding: 0 10px 0px 0" src="/images/angry.jpg" />

I started an adventure into Ionic Framework and Android Studio on a shiny new MacBook Pro today.

[Ionic Framework](http://ionicframework.com/) is a front-end framework for building hybrid mobile applications. Ionic leverages the incredibly successful [AngularJS](https://angularjs.org/) JavaScript framework and [Cordova](http://cordova.apache.org/).

The idea behind hybrid applications being you can take your skills a aweb developers and build fully fledged installed web applications. The other big advantage of of the hybrid approach coupled with the likes of Cordova is you can technically build one application and deploy to multiple eco-systems. IOS, Android, Windows Phone Blackberry and many more.

Uuurrrgghhh!! not such a simple experience so posting the process here in hope it may help someone else. There are a few steps below but excluding download times this is a 5 minute job so please have a go.

## Install NodeJS.

Use [homebrew](http://brew.sh/) or get the [package](http://nodejs.org/).

```
$ brew install node  
```

## [Install Android Studio](https://developer.android.com/sdk/installing/studio.html). Also install your preferred [sdks](http://developer.android.com/sdk/installing/adding-packages.html)

After installation to make Android Studio play nice you need the tools and platform-tools on your path. A [detailed post on how to manage your path](http://coolestguidesontheplanet.com/add-shell-path-osx/), but cheat sheet below. You may be prompted to install Java SDK, Do it

## Create/edit .bash_profile if you don't have one.

```
$ nano ~/.bash_profile
```

## Add the following lines to your .bash_profile to add sdk/tools and sdk/platform-tools to your path

Tip: ctrl-o to save and ctrl-x to exit

```
export PATH="$PATH:/Applications/Android Studio.app/sdk/platform-tools:/Applications/Android Studio.app/sdk/tools"
```

Reload your .bash_profile

```
$ . ~/.bash_profile
```

## Create an AVD (Android Virtual Device) 

This is the emulator to be used for development. You can use the GUI or the command line. First list the possible devices based on installed SDK's. Then create it. More detailed instructions on creating AVD's

```
$ android list targets
$ android create avd -n <name> -t <targetID>
```

## Install Cordova & Ionic Framework (use sudo if you need to) it is simply an npm package

```
$ npm install -g cordova ionic
```

## Create your first app by going to your regular code/projects folder and executing the following

Tip: During this process operations failed as apparently Ant is no longer included in OS X. You can easily remedy that by installing Ant. I found this SO thread useful.

```
$ ionic start awesomeapp tabs
```

## Hop into you app folder

```
$ cd awesomeapp
```

## Add android platform to your application

```
$ ionic platform add android
```

## Build the application

```
$ ionic build android
```

## Finally run it!!

```
$ ionic emulate android
```

## Additional reads

[Installing NodeJS with Homebrew](http://thechangelog.com/install-node-js-with-homebrew-on-os-x/)
[Managing Android Virtual Devices from the command line](http://developer.android.com/tools/devices/managing-avds-cmdline.html)
[Note on boosting performance. Intel have provided an image that dramatically improves performance of the emulator.](https://software.intel.com/en-us/blogs/2014/03/06/now-available-android-sdk-x86-system-image-with-google-apis)
[Modifying shell path on MAC OS X 10.9](https://software.intel.com/en-us/blogs/2014/03/06/now-available-android-sdk-x86-system-image-with-google-apis)

## Feedback

Not helpful? Or if you find any errors please leave a comment or get me on [{{ site.twitter_username}}](https://twitter.com/{{ site.twitter_username}})

photo credit: [Navaneeth K N](https://www.flickr.com/photos/navaneethkn/7975953800/) via [photopin cc](http://photopin.com/)