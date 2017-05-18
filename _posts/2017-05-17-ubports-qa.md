---
layout: post
title:  "UBports Community Q&A: May 13, 2017"
date:   2017-05-13
description: "A lot of news, more questions, and just as many answers."
categories:
---

[![livestream]({{ site.url }}/assets/2017/05/13-openstore.png)](https://youtu.be/s-_L3J6EvgY)

A little late, but here's the summary of [our latest Q&A session](https://youtu.be/s-_L3J6EvgY). Some facts from the video are already outdated, so read on for a slightly edited summary. Enjoy!

## A huge Thank You to our patrons!

- Thanks to everyone who supports us on [patreon](https://www.patreon.com/ubports). We currently have 105 supporters donating a total of ***$1,103***! Your continuous support keeps Ubuntu Touch alive.

## What's been happening?
- Some cool new people joined our marketing team, providing valuable feedback on how to grow the project more efficiently. As a first step, we created a [mailing list](https://bit.ly/ubports) to keep the community in the loop. Be sure to subscribe!
- Brian Douglass implemented [some amazing new features](http://blog.bhdouglass.com/openstore/web/2017/05/02/the-openstore-upgrade.html) on the [OpenStore](http://blog.bhdouglass.com/openstore/ubuntu-touch/2017/05/11/the-openstore-app-upgrade.html) and [its website](http://blog.bhdouglass.com/openstore/web/2017/05/15/openstore-improvements.html). If you have the OpenStore app installed on your device, it can just update itself. If not, it might be a good idea to [install it](https://openstore.ubports.com/docs), since all the cool kids are using it and you don't want to be the one person without the OpenStore. That would be weird, wouldn't it?
- [uNav](https://youtu.be/_ooAoZcGei8) is back! After seeing the amazing community interest in Ubuntu Touch, Marcos Costales decided to bring the [back to the OpenStore!](https://openstore.ubports.com/app/navigator.costales). Give him a high-five, everybody!
- [ubports.com](https://ubports.com) is now pretty! Please give us your thoughts on the new design.
- In a similar vein, [our devices website](https://devices.ubports.com) is also pretty!
- We are looking for testers of our new legacy images on all UBports and official Canonical devices. Please note that these are in alpha state and installing them will wipe your device. If you want to help with that, read [this wiki page](https://wiki.ubports.com/wiki/How-to-flash-existing-ubuntu-touch-devices-with-Ubports-images) and be sure to [report all the bugs](https://wiki.ubports.com/wiki/UBports-Bug-Trackers) you find. Thanks!
- Our [build chain](http://ci.ubports.com/) and [system-image server](http://system-image.ubports.com/) are fully operational.
- All Ubuntu Touch core apps have been forked into GitHub. [The telegram app](https://openstore.ubports.com/app/com.ubuntu.telegram) has already recieved some love from Florian, and it now supports secret chats and voice messages. Supergroups will be supported soon, but there are still some blockers to be fixed before that can be released. [If you want to help us](https://forums.ubports.com/topic/225/core-apps-forked-on-github) with core apps and maybe even pick their further development, we would be really thankful


## Now let's take on some questions!

### Are we going to use snaps?
The plan is to use snaps in our yet-to-come non-legacy branch. We can't decide yet if it will be the only form of delivering packages to the next generation of Ubuntu Touch, but we definitely want it!

### Why aren't the legacy devices listed on [devices.ubports.com](devices.ubports.com) yet?
Since the images are not completely tested, we did not update the page yet. This should happen within a week or so.

### Will there be support for the Nexus 4?
Yes, we have a developer willing to take it on! Since it doesn't have blazing fast hardware, probably only on the legacy branch, though...

### When will there be new ports?
We are currently working on [Halium](https://halium.org), a common base for multiple alternative linux-based mobile operating systems. As soon as that's done, we will think about new ports.

### What's the status of Anbox?
It's under heavy development on the desktop, but we have higher priories right now. If you want to discuss Anbox, you can join their [telegram group](https://t.me/anbox).

### Why is Aethercast/Miracast so bad? You should fix that!
This is a tricky one. It is yet to be decided if there will be further development on this. It's not a very good replacement for an HDMI connection due to massive input lag. Input and help from the community is very much appreciated here!

### What's the future of app-dev on Ubuntu Touch? Are we sticking with QML?
Another tricky one. For now, yes. You heard us talking about limited time and resources, right? That's the reason. We are [evaluating different options for the future of app development and design](https://forums.ubports.com/topic/170/a-vision-of-where-to-go-after-ubuntu-touch-s-death), but this is nowhere near to a decision.

### What are you doing to make sure that no malware gets into the OpenStore?
Not much, at the moment, to be honest. We are not as big of a platform for hackers to target us, but we will have to work on that. Feel free to send your pull-requests to [the OpenStore GitHub Page](https://github.com/UbuntuOpenStore) to help us improving security.

### Are you going to improve Bluetooth Heaset support on Ubuntu Touch?
This should not be too hard to fix, since the bluetooth-stack does most of the support, but it's not very high on our todo list. As always, we're happy to merge any pull-requests.

### Will Halium fix all the hardware enablement bugs?
Yes! Not immediately, of course, but we will get there. First of all, as soon as Halium is released, there is some work required to make Ubuntu Touch work perfectly fine with it. Then, Halium needs to be ported to the specific target device. This is not necessarily less work than porting an operating system to a device directly, but since Halium is supported by multiple projects, there is a much larger crowd to collaborate on the port.

### Does Halium create compatibility with apps for other operating systems?
No, that's not what halium is. It's just a standardized way of making android drivers usable from within other mobile operating systems. We also want to collaborate with other projects on app-dev, but that remains a thing for the future. Baby steps. We will get there.

### What's happening with convergence?
Convergence is awesome! We want it. It's our selling point, and we would like to embrace it in the next generation of Ubuntu Touch.

### Please elaborate on what the 16.04 image will be.
Well, it's going to be based on Ubuntu 16.04 (suprise!), which is very important for us, since we can still benefit from Canonica'ls support that way. The legacy images are still based on Ubuntu 15.04, so we would have to do a lot security maintanence if we're stuck with it. There will be Snaps, Halium, and Systemd. Other than that, no decisions have been made yet. It mostly depends on what the community wants to see (and what's feasible)!

# We need your feedback!
We would like to hear your opinion on what you want the next generation of Ubuntu Touch to be. Obviously we can't be everybody's darling, but since UBports is a community-funded project, we need to know your whishes for the future of the operating system. Please use [this forum thread](https://forums.ubports.com/topic/229/what-is-your-main-points-for-a-perfect-personal-phone-operative-system) for discussion.

You still have questions that haven't been answered yet? No problem, our next Q&A will happen on Saturday, May 27 at 6 PM UTC. If you won't be able to catch us live, be sure to get your questions in beforehand in the comment section down below or [the forum](forums.ubports.com).

That's it for this time, make sure to [catch the next one](https://www.youtube.com/watch?v=517OFPd_VTI). If you want to discuss this or tell us how stupid we are, you can do that on the [UBports forums](https://forums.ubports.com) or in [our Telegram supergroup](https://ubports.com/telegram).

Take care and have a good one!

-Dalton and Jan

P.S.: Be sure to [subscribe to our new and shiny mailing list](https://bit.ly/ubports)!
