---
layout: post
title:  "Stable OTA-1, Halium is Heating up, Convergence Works!"
date:   2017-06-14 07:00 -0500
description: "The UBports team releases OTA-1, talks about Halium, takes some questions, and asks for help with maintaining the core apps"
categories: QandA
---

[![Ubuntu Touch 16.04 in Windowed Mode](/assets/2017/06/14-Convergence.png)](https://youtu.be/g3bIrfqmMek)

It's been another great couple of weeks, and we had a lot of news to tell you all about during our [latest Community Update](https://youtu.be/g3bIrfqmMek)! Read on to discover all of the juicy details!

## Thank you to Patreons and Sponsors!

We want to take a bit of time to thank all of our [Patrons](https://patreon.com/ubports) and [sponsors](https://ubports.com/sponsors). You are all proving to us that what we do is important and useful to the wider community. Thanks for sharing the ride with us. If it wasn't for you, we wouldn't be here.

---

## The News

### Stable OTA-1 is shipping! (except the Nexus 4 and 5)

The UBports project is proud to announce Stable OTA-1 for all of our officially supported devices, minus the Nexus 5 (hammerhead) and Nexus 4 (mako).

This was the most exciting news for us. OTA-1 is the culmination of our efforts over the past two months. It brings many bug fixes and enhancements to the platform, including:

* Experimental AGPS support
* The UBports Welcome app
* The amazing OpenStore
* Terminal and File Browser are preinstalled (It's the little things!)

As well as bug fixes for the UBports ported devices. You can see a list of bugs targeted and closed for this release [here](https://github.com/ubports/ubports-touch/milestone/1?closed=1).

The Nexus 5 will be receiving the update shortly. A last-minute regression found in the battery meter caused us to pull the update. The Nexus 4 is being brought up separately from the rest of the devices and its OTA-1 release will be announced when it is ready.

### OS/App Developer Meeting

On June 1st, we invited about 20 Ubuntu Touch App and Platform developers to a meeting where we discussed how we can do things better in the future. A lot came out of this meeting and we'd love to discuss all of it here, but there's a much better write-up [in our forum](https://forums.ubports.com/topic/273/june-1-2017-app-developer-os-developer-meeting/14).

These were some of the big discussion points:

* Snaps may be a good addition to the platform, but we'll need to make modifications to snapd before we can use them
* To service notifications in the future while improving user privacy, we will implement "headless apps". The OS will call these every few minutes and allow them to do some work in the background such as check for messages. This will be done with battery savings and user control in mind.
* We would really like to have the newest features in Qt 5.9 available to us, such as QtQuick 2. This will require Yunit to be built with Qt 5.9, which was not officially packaged in 16.04 at the time of the meeting. More discussions are happening on this.

### Halium is Moving Quickly

Halium, as you may know, is a project aiming to standardize the Android hardware compatibility layer between many Linux distributions. This layer is required because Android drivers can't be used natively in a regular Linux distribution. This week the project had a lot to show off - it can boot both Ubuntu Touch and Plasma Mobile. 

As you can see in [this tweet](https://twitter.com/HaliumProject/status/871592584136622081), Halium can boot both OS's on the Nexus 5. The third image, though, is the most interesting. It shows Plasma Mobile booting on the Fairphone 2, a phone that the OS hasn't been explicitly ported to. It's easy to see the opportunities that Halium opens up and we're proud to be a part of the project.

### We have a Public Roadmap!

Okay, it's still a work in progress, but you can see the goals that we're setting for every release on [our ubports-touch milestone tracker](https://github.com/ubports/ubports-touch/milestones). This lets the community see what we're targeting to cut a release. The 16.04 milestones are still filling up with enhancements, so stay tuned!

### Marius showed off Convergence

At this point in the update, Marius took out his trusty Nexus 5 and Slimport cable to show off convergence. It's a little difficult to see his screen, but you can find this at [38:00](https://youtu.be/g3bIrfqmMek?t=38m0s) in the video.

---

## Questions and Answers

With all of our news out of the way, we began taking questions from the community.

### Is the branding staying the same? Will we keep the Ubuntu Touch and UBports name?

We're carefully weighing our options on changing the name. We have nothing more to say on this topic right now.

### What will happen to the Nexus 7 2013 WiFi (flo)?

This was a device that Canonical provided an image for, but we don't yet have one available. We do not have a test device available. Also, our developers have a lot of projects going on right now. If you'd like to try porting Ubuntu Touch to this device yourself (and don't want to wait for Halium and 16.04-based images), please check out our [forum](forums.ubports.com) to collaborate with others.

### Can you make a guide that makes it easier for people to choose a channel to flash?

[Sure we can!](https://wiki.ubports.com/wiki/Release-Channels)

### What's happening in our collaboration with Yunit?

Yunit is [working on backporting its stack to 16.04](https://forum.yunit.io/viewtopic.php?f=5&p=215#p215) since it's only running on Debian Unstable and Ubuntu right now. That'll be really helpful.

### What's the status of the switch to UBports script?

It's just a proof-of-concept for now, but if you want to try it, [knock yourself out](https://github.com/mariogrip/switch-to-ubports). It might be integrated into the UBports installer in the future.

### What does Google's Project Treble do for UBports and Halium?

Google recently announced "a modular base for Android" to solve the problem of having to backport Android updates to every device seperately. While Treble does sound similar to Haliums approach, it doesn't eliminate the need for Libhybris, the translation library for Android's bionic drivers. It remains to be seen if this project will change our life for the better, but since it's just been announced, we can just continue what we're doing at the moment for now.

### What's happening with Anbox?

We definitely want Android App compatibility, but it is not our highest priority for the moment. Since there's so much to be done, it will also probably not land for 15.04, but we're looking forward to playing around with it on the soon-to-come 16.04 images. It is important to point out here, that we still need top push for native apps. Anbox will just be a way of getting crucial android apps that don't exist on Ubuntu Touch otherwise to run, similar to Wine on the Linux Desktop. The experience will probably not be the same, but it will help eliminate the immediate need. Apps like WhatsApp, Snapchat or Netflix will probably not be ported to Ubuntu Touch, so it makes sense to run them in Anbox if it's possible.

### Why is Anbox needed? Can't you just use Dalvik from the Android container?

It's not that simple. This would require us to build compatibility with the Mir display server and all of the userland, it doesn't work like that.

Also, **we don't want to be android!** We want Ubuntu Touch to be a GNU/Linux distribution for mobile devices, the Android container is just the way for us to get hardware access and we don't want features to depend on it.

### What's the first feature you will add to Ubuntu Touch?

Well, we already archieved a lot. Agps, bug fixes, minor UI improvements, updates on the core apps, etc. A big jump will be of course the transition to 16.04 and with it the upcoming snap support, but if you're looking for features from a user perspective, it will probably be Anbox and .apk support.

### Is it possible to use the Ubuntu UI toolkit on 17.04 to develop apps?

Not right now, and we don't have the resources to make it work right away. If you don't want to use 16.04, you can [run it inside an LXD container](https://wiki.ubports.com/wiki/Set-up-a-Clickable-working-environment-inside-an-LXC-container) to create your apps.

### Will UBports ever come to closed-source devices?

No. The device tree needs to be open-source, so the porters can see what's happening underneath. Ubuntu Touch on the iPhone is not going to happen.

---

## Calls for Help

We always get people asking "How can I help you guys out?" Well, here are a few things that we'd really appreciate!

### Marketing

Our marketing team is working to bring you guest blog posts, interviews, and behind the scenes snapshots of all those involved in making this project possible! If you'd like to help the UBports Marketing team spread the word about our wonderful OS, fill out the form [here](http://bit.ly/ubportsmarketingsignup)

### Core App Maintainers

We're looking for help maintaining our Core Apps. If you'd like to learn about developing for the Ubuntu Touch platform, check out the list of apps [here](https://github.com/ubports/?utf8=%E2%9C%93&q=-app&type=&language=) and pick one you like! There's also a guide to setting up Clickable, a development environment for Click apps, [here](https://wiki.ubports.com/wiki/Set-up-a-Clickable-working-environment-inside-an-LXC-container). Be sure to get a hold of us on [the forum](https://forums.ubports.com), we have a developer community that's happy to help!

### Spread the word!

Tell everyone about UBports! We're going to be more active on our social media in the coming weeks, so be sure to check out our [Twitter](https://twitter.com/ubports), [Mastodon](https://mastodon.rocks/@UBports), and [Google Plus](https://plus.google.com/+UBports) accounts.

---

Well, that's it for this time! Thank you again to everyone who has contributed their time, money, and excitement to our project! We'll be back in two weeks with [another community update](https://www.youtube.com/watch?v=0BoiGoXrVCo), as always! In the meantime, you can get a hold of us on [our forum](https:forums.ubports.com), [Telegram supergroup](https://ubports.com/telegram), or #ubports on Freenode (which is bridged to that Telegram channel).

