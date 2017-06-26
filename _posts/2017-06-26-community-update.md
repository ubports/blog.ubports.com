---
layout: post
title:  "Core Apps, Backup Script, and a New Website"
date:   2017-06-26 14:00 -0500
description: "On our June 24, 2017 community update, we talked about "
categories: QandA
---

Our latest Community Update was on June 24, 2017. If you'd like to watch the video version, you can find it [here](https://www.youtube.com/watch?v=0BoiGoXrVCo). These sessions typically occur every two weeks at 1800 UTC so come along next time if you have a question. You can also catch up on previous ones on [our youtube channel](https://www.youtube.com/channel/UCDGJ7jdEoOx6_o_GbkjFaBg).

Two weeks have already passed since our last Q&A and a huge amount of behind-the-scenes work here at UBports. Whilst many of the behind-the-scenes updates listed below are not immediate in their impact they are all critical not just for sustaining existing progress but also for the eventual development of new builds for new devices. Some developments like those of of Halium and Core Apps, although currently invisible, will lead to a much smoother, better mobile operating system in the future. We're pleased with the progress and excited to share it with you below along with updates from Halium, Core Apps Update, Backup Script for devices, Ubuntu 16.04, our new website, sponsor news and updates about the UBports Foundation.

Before we begin, as usual, we are honoured to take a moment to thank all of our sponsors. Our [Patreon](https://www.patreon.com/ubports) (public voluntary donations)  reached $1800 per month today - a staggering amount for a project that was just a 'garage band' three months ago. Thank you all for voting and encouraging with your wallet, telling us that our mission is important.

Recently, we've been discussing what we could do with the revenues beyond paying developers. One idea being considered is having an "app dev" fund where we buy and ship budding developers a device to help them make their app.

We'd also like to thank our largest sponsor, [Smoose](https://smoose.nl). Smoose is a Dutch IT services company focused on making the workplace more open (source). They've made a lot of our work in the past year possible by distributing phones to developers, sending us to events (MWC was really cool!), and generally offering support wherever possible.

### Halium 7.1

Halium is one of the fastest-moving projects that the alternative mobile OS community has seen lately. Halium is a common platform for running GNU/Linux distributions on Android phones.

It started just two months ago with "Hey, all of our projects use the same library and we should make it standard." Now, it is to a point where it is able to boot Ubuntu Touch 16.04 and Plasma Mobile on devices with Android 5.1. Today, Marius announced another huge leap for the project: budding Android 7.1 support.

The code for Halium 7.1 has been released on [Halium's GitHub organization](https://github.com/Halium/android/tree/halium-7.1). It is to a point where developers can build it and flash it to a device with ADB debugging. Most hardware isn't working yet, but getting to the debugging point is an important first step for Android devices.

More info about Halium can be found on [their website](https://halium.org/)

Many people have noticed that we've been pouring a lot of development time into Halium rather than the Ubuntu Touch system itself. This is because we need a stable system underneath Ubuntu Touch before we're able to continue developing it. When debugging software, it's important to know that you're going to get the same results every time you run it. Halium gives us this peace of mind.


### Core Apps

Thank you to all of our community members who have been contributing to the Ubuntu Touch core apps. These are those apps that were mostly originally developed by Canonical or partners, but still need updating to keep them running smoothly and securely. There have been many pull requests sent applying to the Gallery, Clock, and Keyboard with many more coming in daily so the promise of updates and fixes for the future is strong.

Some of the (still unreleased) changes include:
    The Gallery app allows you to zoom in further to your photos
    The Clock app has some UI tweaks (it also nuked its automated build environment, which was fun.)
    Lots of translation improvements

We've also been focusing more of our concerns on localization. Ubuntu Touch must be made as accessible as possible to people around the world, in their native languages. Canonical was able to use Launchpad to perform translation, but we don't have that hooked up quite yet. If you have any suggestions or input on software that makes your life as a translator easier, let us know in [this forum thread](https://forums.ubports.com/topic/386/localization-software-evaluations).

We're also looking at ways to set up our build server so it becomes even more automatic using Jenkins pipelines. These will automatically build any pull requests that you send in to our GitHub app repositories, enabling us to make faster and more useful decisions on merging code.

This is a prime example of the free and open software community really stepping up to further a project that they care about. We appreciate your support.

### Backup Script

Florian (@flohack) has written an excellent little script that helps you back up and restore the data on your phone. This will be really handy if you're switching from the Canonical build to the UBports one. 

Be aware, some system settings like saved Wi-Fi networks are not backed up. We also don't back up the apps that you have installed, you will need to grab those again under the new install. We don't have an exact list of what you'll since it isn't really clear where UT stores all of its settings, or how to restore them. A good rule of thumb is that you'll keep all of your data, keep most of your app settings, lose your system settings.

The script has been integrated into [Marius Quabeck's magic-device-tool](https://github.com/mariusquabeck/magic-device-tool). We'd love if you tried it out on your non-main device and gave us your feedback!

### Marius talks about 16.04 for a while

A lot of work is happening on the low-level bugs in the 16.04 version of Ubuntu Touch. These are bugs that prevent us from releasing any 16.04 images to the community. Stay tuned!

### Our New Website

[Smoose](https://www.smoose.nl/), the main sponsor of UBports for some time, promised to give us a new website while we were at Mobile World Congress earlier this year. This week, they delivered on that promise. 

Our new website, based on Odoo, looks and works better than anything we've ever had. We love it and we hope that you do too. If you have feedback, our marketing team would appreciate it. You can fill out the feedback form [here](https://ubports.com/survey/start/website-feedback-needed-4).

Tangentally, our marketing team is working on putting all of our social media accounts in one feed so they can answer questions faster. They also created an account on Diaspora* (ubports@diasp.ca).

### Security Discussion

We received a forum post recently asking how we are handling security. Generally speaking, this is how we are protecting your phone:

System images are GPG signed and verified on your device. You can learn more about this process [here](https://wiki.ubuntu.com/ImageBasedUpgrades/GPG)
Apps in the OpenStore go under manual review if they request a certain set of permissions. This means that a real person looks over the app to make sure it's safe before anyone can ever download it. You can read more about the submission and review process at [the OpenStore's Submit page](https://open.uappexplorer.com/submit)

### UBports Foundation

This is the big news that we were teasing everyone about leading up to the Q&A. It has finally gotten to a point where we are ready to make the announcement 'official' in the most basic sense of the word.

Therefore, UBports project presents... The UBports Foundation! (*Insert symphonic hit and crowd cheering sounds here*)

The UBports Foundation is a German non-profit entity (stiftung)created with the purpose of furthering the Ubuntu Touch platform. The way that this entity achieves this goal is to be decided by its board, but in general it will allow UBports to perform the following actions:

* Collect money (Tax deductible for all you Europeans!)
* Spend money 
* Negotiate contracts as a legal entity (This will make more sense as time goes on)
* Provide transparency of usage of funds 
* Provide transparency in decision making

Community contributors will be able to apply to become voting members of the Foundation, and be able to democratically elect the Board of Directors. The application process isn't going to be 100% painless (sorry to drive-by contributors). We'll go with 90% painless. We're taking the project seriously and we want the team to do so as well. Therefore, we must have some processes and audits in place.

Unfortunately, we aren't comfortable sharing the Foundation's founding documents quite yet as they have information about sponsorships and agreements that aren't fully settled. Stay tuned and we'll bring all of this to light.

### Community Questions

At this point, we took some questions from live chat and things we've been seeing around the community

#### For app development, should I learn QML or C++?

You should learn both. QML is good for some things, but C++ really pulls the language together on the Ubuntu Touch platform. There are also some Python bindings found in PyOtherSide that can make development easier if you know Python.


#### Can you make apps that run on Plasma Mobile, sailfish and UT?

Plasma Mobile runs UT apps. It shouldn't be too hard to go the other way. Sailfish, on the other hand, has some pretty custom things in their OS (not to say that Ubuntu Touch does not) that cause some problems.

So, if that wasn't wishy-washy enough for you, the answer for Sailfish apps is an honest "We don't know."


#### Will you port to the OnePlus 3 and OnePlus 5?

This was a funny question to receive during live chat after we had just said "We're not porting to new devices" earlier in the video.

However, the answer probably isn't quite what you expect. The OnePlus 5 has become one of Halium's unofficial official testing devices for Halium 7.1, so... yes. We will have Ubuntu Touch on the OnePlus 5.

And at the same time, OnePlus 3 was also used to test Halium 7.1, This was used before OnePlus 5 was released as an debug device, so expect this device also.

When will it be released?  "It'll be released when it's ready."

#### Hey! You have bugs in your bug trackers for 15.04! Will you fix them?

It depends. We're balancing our time between 15.04 bugfixes and 16.04 bringup. 15.04 is such a buggy and unsupported platform that we'd really love to run from it as quickly as possible.

For everyone with the Legacy devices, we're keeping the lights on for you. We're not going to make your experience perfect, though.

Tangentially, we'd really love for some UI/UX designers to join our team. Drop us a line if you've got great ideas for the platform!

#### How is the tablet OS going?

The OS is the same between phones and tablets. Progress on one side is progress on the other. Convergence!

#### You should fix the long boot-time bug on the M10 FHD.

We need a developer that is willing to dedicate the time to tracking down and fixing that bug. At the moment, it rates pretty low on our list of priorities. The long boot time is inconvenient when you need to reboot your tablet, but it isn't experience-shattering.

#### Why aren't all devices getting 16.04?

A few reasons:
    Some of the old official devices are too low-end and can't show off the Ubuntu Touch platform. Would you rather show off your favorite GNU/Linux distribution running on a sleek, new computer or a 2007 one? Which will get you a better crowd response?
    All of the old official devices are closed-source so we can't fix hardware enablement issues
    16.04 requires Linux kernel 3.10 at a minimum to function
    We don't have the resources to support all of these devices, especially considering the manufacturer of their chipset

If you'd like to maintain these devices into the 16.04 transition, we will support you as much as we can. We can't guarantee that the work will be fruitful, though.

-----

That's all for this week! We hope you enjoyed our action-packed Update as much as we did. We'll see you for the next one on July 8, 2017 at 1800 UTC!
