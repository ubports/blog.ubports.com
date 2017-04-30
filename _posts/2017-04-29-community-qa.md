---
layout: post
title:  "UBports Community Q&A: April 29, 2017"
date:   2017-04-29
description: "Some news, some questions, some answers."
categories:
---

[![livestream]({{ site.url }}/assets/2017/04/29-dalton.png)](https://youtu.be/UvfeCj6SRGg)

Another fortnight, another Q&A session! Watch it [here](https://youtu.be/UvfeCj6SRGg) or read on for a quick summary.

What's been happening?
--------------------------------------

- First of all, a big thank you to all our [Patreon](https://www.patreon.com/ubports/posts) supporters. We are currently recieving just over 600$ in donations every month, so this helps a lot in making UBports sustainable. A big high five for that!

- [Halium](https://halium.org/) is in the air! We joined forces with the Plasma Mobile and Sailfish OS community to create a common base for non-android Linux-based mobile operating systems. We will basically create a unified way of implementing Libhybris, a library that allows us to directly address the Android hardware abstraction layer (HAL). That way, the future of porting will be making Halium work on a device and then just installing any mobile operating system that works with it. A prototype on the Nexus 5 is in the works right now, and it's gonna be *great*! Bright future ahead, everyone!

- The development team has been working towards building a custom Ubuntu 16.04 rootfs. To make that possible, we now have two extra ARM-servers to speed up compilation.

- We are aware that the community wants to see an official roadmap. That is already in the works and will be published soon.For now, you can go stalk us on on our [trello boards](https://trello.com/ubports), even though some project management resources still need to be moved there.

- A new website is in the works! Look out for that next week.

- We now have some further insights into Canonical's plans: The official devices will receive security-updates until the end of June 2017 (We will of course release new images before that) and the click store will stay open until the end of this year. We might even keep it in the images for now, so have a little less pressure to create a seamless transition. We will eventually move all the free and open-source apps to the [openstore](https://openstore.ubports.com/).

## Call to ARMs

Yes, pun intended. No, I am not sorry. We know that the community is eager to help us and we apologize that we don't have the resources to enable you to do that. But we actually have a few things that we can use your help with right now:

- We need a decent **build management tool**. We're looking for a tool that hooks into our system image server and let's us promote builds from our development channel to the slower-moving channels. There is no requirement on language for this, though Marius might kill us if we accept PHP.

- If you know **Groovy** and have some experience writing plugins for **Jenkins**, please get in touch with us! We are looking for a way to automate taking on new devices. Your program will need to check a GitHub repository for files and take build instructions from them.

- You're a **web designer** and you know **NodeJS**, **Pug** and **Bootstrap**? Awesome! Care to look at our [website redesign](https://github.com/ubports/ubports.com/tree/mariogrip/new-design)? Just make it look good, that's all we ask for. ;)

Thanks for your help, now let's answer some questions!

Q&A
-----------------------------------------

### What's going on with the Station Dock?

At Ubucon Europe last year, we announced a nifty little device called the [Station Dock](https://blog.ubports.com/2016/11/22/new-shiny.html), a Raspberry Pi based gadget that helps with convergence on devices that don't have wired HDMI out. While there is a working prototype and everything would be ready to go, managing a Crowd-funding campaign and building hardware is a lot of work and we are unsure if _more work_ is what we need right now. We yet have to decide if we want to follow through with the campaign or just open-source the plans and software right away.

### What about the stable builds? You said they were going to be published this week?

One thing that we'll have to do in the future is tell the community when we are going to be able to meet deadlines like that, and in this case we are not. There are still [some bugs we want to fix before release](https://wiki.ubports.com/wiki/UBports-Bug-Trackers), so there is a little delay. An unstable stable release would be a little weird.

### What is "Legacy Mode," and why are the old official Canonical devices included in it?

The older devices will be on life support and the actual work will happen in the non-legacy branch, but we will still provide critical security-updates and merge bug-fixes from the community. This way you will still be able to use your phone with Ubuntu Touch if you own one of the official devices, but the cool and shiny new features will probably only land in the non-legacy branch.

We are putting devices here because we don't have any other choice. The official devices from BQ and Meizu have closed Android device trees. Because of this, we aren't able to fix bugs in hardware enablement or add new features dependant on the kernel.

### When will I be able to reflash my phone?

We're working as fast as we can. Hopefully the new images will be out there in one or two weeks. We managed to get some blockers out the way and are working on it.

### Will the Nokia HERE AGPS service stay in the builds for the former official devices?

There's still a question mark there due to licensing issues. If we are allowed to keep HERE, it will stay in the builds, if not, we will try to replace it with Mozilla AGPS.

### Will you take over the existing bugreports from launchpad or does everything have to be reported again?

We won't touch that before we have to, because we don't want to break all the links and we really don't want to report everything again. Some may be moved in the future, but that's yet to be decided.

### What will happen to the application lifecycle restrictions of Ubuntu Touch?

It's too early to decide that yet, once there are new images, we will think about that.

### Will you host the Ubuntu Touch documentation on you own wiki or will that stay where it is right now?

For now it will stay in the Ubuntu Wiki, and if we're not forced to move it we won't. This may change in the future, though. Limited resources, you all know the story.

### Will you support MultiROM?

Probably not. We haven't played with MultiROM in over a year and it would be too much work to fix it right now, so if you have MultiROM and you want Ubuntu Touch, you will have to choose one OS. That ¡\**may*\*! change with Halium, but that's not carved in stone yet and we won't make any promises.

You still have questions that have not been answered yet? No problem, our next Q&A will happen on Saturday, May 13 at 6 PM UTC. If you won't be able to catch us live, be sure to get your questions in beforehand in the comment section down below.

That's it for this time, make sure to [catch the next one](https://www.youtube.com/watch?v=s-_L3J6EvgY). If you want to discuss this or tell us how stupid we are, you can do that on the [UBports forums](https://forums.ubports.com) or in [our Telegram supergroup](https://ubports.com/telegram).

Take care and have a good one!

-Jan
