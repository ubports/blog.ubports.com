---
layout: post
title:  "UBports Developer's Meeting - March 29, 2017"
date:   2017-03-30 15:50:00 +0000
categories: 
---

![conferencecall]({{ site.url }}/assets/2017/03/30-conferencecall.jpg)

Yesterday some users and developers from UBports got together online to discuss the project's present and future goals. There was fun discussion, everyone's drinks of choice (for all members for which it was legal), and plenty of cats in the webcam frame. We spent some time on a few topics that should be interesting to the community at large.


## Device Status

Our focus right now is on our three stable devices: The FairPhone 2, Oneplus One, and Nexus 5. We're putting our efforts toward bringing these devices back to a fully working state. After that's finished (which it is, mostly), we will push an image to the Stable channel. Gone will be the days where development channels are more functional and less buggy than stable! Prepare thy phone!

### Oneplus One

I don't have too much to say about this one. The developers working on this device have been pretty quiet in the UBports Telegram chat, so I haven't heard about it.

### Nexus 5

A few dedicated community members ensured that the Nexus 5 is ready for prime time once again. We're going to push a new build to Stable for this device very soon.

### FairPhone 2

Same story as the Nexus 5, but with a much larger community. Thanks to the support of Smoose (a Netherlandic technology company), we were able to bring this device to a stable state in record time. In this process, we fixed quite a few blocking bugs for the Oneplus One and Nexus 5. A shared base means something!

## Near Future Goals

### Bug Reporting

This has been a sticking point for users and developers alike. We've decided that *all* bug tracking for UBports devices will take place on Launchpad. See the [Get Involved](https://ubports.com/get-involved) page for more information. Feel free to report bugs in UBports websites in their GitHub repository.

### Polish

The next few weeks will be spent on polishing our stable devices before shipping an image to the Stable channel. After that, we'll move on to making the websites and wiki nicer. We hope that you'll love how everything looks!

## Farther Future Goals

These come after the near future goals.

### New Base

It's no secret that an Android 5.1 (CyanogenMod 12.1) base limits us from porting Ubuntu to new devices. Because of this, we will begin work on a LineageOS 14.1 base. This doesn't mean that current devices are abandoned, it will simply lay the groundwork for future devices.

### New Ubuntu

Ubuntu 15.04 is almost entirely abandoned. Full stop. The only updates that Canonical has promised are for security. We need to move on from 15.04 as soon as possible. The 16.04 Touch images seem like a good place to jump, even though they aren't currently functional. This will give us a platform that's able to run Snaps *and* Clicks, allowing us to move on to Ubuntu Personal when it comes around.

We've decided that, if possible, the FP2 will be our Ubuntu 16.04 testing device. We need to get snapd running on it first.

### New Device

This is where we had the least success. Our dream device for porting Ubuntu and showing it off meets a few requirements: it has MHL, Slimport, or a dedicated HDMI port; it is available in the US as well as the rest of the world (official Ubuntu devices got the second part right); and it is powerful enough to make convergence shine. The Galaxy S8 announcement came at the perfect time, we're just interested in how friendly Samsung will be to developers.

If you have any suggestions for this miracle device, we're all ears in our Telegram group (you can grab the link from the MOTD of #ubports on Freenode for now).

## Other Things

We'll be removing the devel_rc-proposed channel soon. Four channels is a ridiculous amount for a project of our size. System-image-server has the ability to redirect a device to another channel without user intervention, so there's nothing you'll need to do.

Finally, Even though https://stats.ubports.com/ can't be guaranteed to be accurate, it is still an impressive look at the dynamics of our project. With just a small team of developers and a hefty amount of word of mouth, we've gotten really far. Thank you for your support.

-Dalton
