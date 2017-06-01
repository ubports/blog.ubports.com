---
layout: post
title:  "AGPS, App Updates, Halium, and more!"
date:   2017-06-01
description: "A lot of news, more questions, and just as many answers."
categories:
---


[![Ubuntu 16.04 running inside Halium]({{ site.url }}/assets/2017/06/01-xenial-halium.png)](https://youtu.be/517OFPd_VTI)

We had our latest Community Update and Q&A on May 27th. You can watch it [here](https://youtu.be/517OFPd_VTI). There were lots of news stories and questions to go through, so we'd better start!

## The News
 
There's been loads happening with UBports the past two weeks. We've landed new features, gained new sponsors, and seen lots of work by lots of people in our growing community. It is worth remembering that is still just 2 months since the news came of Canonical moving away from Unity and Ubuntu Touch and now we are seeing more activity on Ubuntu Touch than for a very long time and that is really encouraging.
 
### Patreon hit $1500

As usual, we have a lot of Patrons to thank. You all make UBports possible, month after month. As a direct result of your support...

### Marius Gripsgard began working full time

Starting this week, Marius is working on UBports full time which will have an enormous impact on our project! We're taking advantage of this opportunity to plan vital meetings to help progress our growing OS and plan its future using the core teams and long-term Ubuntu app developers. All meetings will be written up and the notes will be shared with the community to keep everyone in the loop.

### UBports Gains a sponsor!!

We were overjoyed and surprised when Private Internet Access (https://www.privateinternetaccess.com/) contacted us offering their sponsorship. We're still reeling that such a huge name in privacy services was willing to put money on the table and tell us that they like what we're doing. 

We will be using the funds from their sponsorship to target directly our priorities with Ubuntu Touch and raise bounties to get developers involved with providing fixes. We'll be deciding these priorities for instance in some of our upcoming meetings. Stay tuned for that.

### All devices that were sold with Ubuntu for Devices can now run UBports' builds

Every official Canonical Ubuntu Touch  device (except the devices that needed to be flashed by users, like the Nexus 4 and 7 2013 WiFi) are now  working with UBports Ubuntu Touch images. This is great news for everyone that was initially worried by Canonical's decision. The image for the Nexus 4 is still under development and we currently don't have a test device for the Nexus 7, but we will hopefully get there soon.

If you would like to try out the UBports images, the please check out how on our wiki (https://wiki.ubports.com/wiki/How-to-flash-existing-ubuntu-touch-devices-with-Ubports-images). There is information on backing up your phone and flashing it with the UBports images (the process will wipe your device's data, so be aware and warned!). We will next create a script that will flash your phone  without data loss so you may wish to wait until that is completed. You can follow progress on this script [on GitHub](https://github.com/mariogrip/switch-to-ubports/blob/master/switch-to-ubports.sh). This is great news for UBports as in less than 2 months we can boast that our devices we support have grown from 3 key devices (Nexus 5, OnePlus One and Fairphone 2) to 13!

### AGPS Mozilla Location Service

As some of you may know, we can't use HERE Maps Assisted GPS included in official Canonical images. Assisted GPS (AGPS) is a system that allows a device determine its location by triangulating the distances to different cellphone towers and WiFi base stations. This method is a lot faster than GPS and can be combined to a very reliable positioning system. We are currently testing our very own implementation of the Mozilla Location Service on Ubuntu Touch! Good job, devs! Again another first for Ubuntu Touch.

### New channels

We are moving to a six-channel system, three for 15.04 (containing the so-called legacy images based on Ubuntu 15.04) and three for 16.04 (not live yet, will contain images for the core devices based on Ubuntu 16.04 LTS). Inside these categories there will then be called  `devel` ([Continuous integration](https://en.wikipedia.org/wiki/Continuous_integration) builds that are automatically pulled from GitHub; these are prone to be very unstable), `rc` (release candidates that are manually promoted from the `devel` channel after successful testing; fairly stable) and `stable` (official releases; as stable as possible). This system will allow us for easier quality assurance and a smooth transition to the new base for the core devices. So 3 channels for 15:04 and 3 for 16:04.

For daily driver use, the `stable` channel is recommended, but we are planning to publish OTA updates more regularly than Canonical used to provide them to ensure all users get the new features and fixes as quickly as possible.

### Bug reporting moved to GitHub

You spoke and we listened: Launchpad is a powerful tool, but it's far from being user friendly, so Jan moved [all the bug reports to GitHub](https://github.com/ubports/ubports-touch/issues). If you're interested in reporting bugs or filing enhancement-proposals, check out [this handy guide](https://wiki.ubports.com/wiki/Writing-a-Good-Bug-Report) that Dalton wrote. You can also track the progress of development on the [Kanban Board](https://github.com/ubports/ubports-touch/projects/).

We will probably still use Launchpad for Translations when we get around to it but that has not been set up yet.

### Halium is coming along nicely

Marius and Bhushan made some great progress on [Halium](https://halium.org). It is now able to boot Ubuntu 16.04 with a basic Android container (see the image above)! Before anyone gets too exited, though, we need to be clear that we still have to complete a lot of work before it's ready to install on consumer devices.

Many things are already working, though. Most importantly, adb and ssh can be used for debugging. Mir, WiFi, Bluetooth, sound and voice calling are already functional, so we might see some builds on the 16.04 development channel soon.

### Backup and restore script

Many people are afraid of reflashing their device to UBports as they fear losing their data, so Florian has kindly been working on making backing up Ubuntu Touch installations easier. It will be integrated into [Magic Device Tool](https://github.com/MariusQuabeck/magic-device-tool), but it's not thoroughly tested yet so again watch this space.

### Dekko is back!

Dan Chapman announced that [he will continue his work on the Dekko E-Mail client](https://forums.ubports.com/topic/228/dekko-as-click/14) on Ubuntu Touch! Due to the imminent deprecation of Click packages under Canonical, he stopped his work on the click version a few months back to focus development on a snap version using a different version of Qt. But the huge community interest in Ubuntu Touch we've seen over the last two months has motivated him to bring Dekko back to the OpenStore so that it will even run on Legacy Devices. This is excellent news for any Ubuntu Touch user.

He will still need some time to iron out the remaining issues, but we can really speak for the whole community when we say **thank you Dan!**

### Rehosting Core-Apps

We are looking to bring the core apps to the OpenStore, but we need maintainers for each one.

We announced earlier that the App-Dev team has been looking into rebasing the Telegram App to Cutegram. As it tuns out, this is not that easy, so the team will instead continue to work on the current stack. Supergroups are still a work in progress, but two-factor-authentication is now working.

### UBports Installer and magic-device-tool GUI

Soon there will be two GUI methods to flash your phone with Ubuntu Touch: The UBports Installer and Magic Device Tool.

The UBports Installer offers a simple experience: plug in your device, start the tool, pick your channel, and press Go. The installer is not ready for use yet, but its **prerelease** code can be found [on GitHub](https://github.com/ubports/ubports-installer). The target platforms are MacOS and Windows, though it also works on Linux. [Check out the video for a live demo](https://youtu.be/517OFPd_VTI?t=1778).

Marius Quabeck's Magic-Device-Tool, on the other hand, is a powerhouse in disguise. It allows you to install many different operating systems on your phone with a few simple steps. The team behind the script is working on a Qt-based GUI to make flashing even easier. For now, you can download the script [from GitHub](https://github.com/MariusQuabeck/magic-device-tool) or install the snap using `sudo snap install magic-device-tool --devmode` (make sure to read the GitHub README!). Please ask in the MDT telegram group if you have any questions or need support.

### UBports in the media

Apart from all the articles being published about UBports around the web, some team members have been interviewed on various shows and podcasts in the last couple of weeks:

- Marius Gripsgard (@mariogrip) and Bhushan Shah (@bshah) about Halium [on the Luduke Hour](https://youtu.be/Sp-K-0NROf4) (English)
- Brian Douglass (@bhdouglass) about uAppExplorer and the OpenStore [on the Ubuntu Podcast](http://ubuntupodcast.org/2017/05/26/s10e12-needy-expensive-spiders/) (English)
- Jan Sprinz (@NeoTheThird) about UBports in general [on the UbuntuFun.de Podcast](http://ubuntufun.de/2017/05/ubuntufun-podcast-folge-35-was-gibts-neues-bei-ubports/) (German)
- Marcos Costales (developer of uNav) about uNav [on Ubuntu y otras hierbas](https://youtu.be/41IUhcPJgrk) (Spanish)

### LoquiIM needs your help!

[LoquiIM](https://openstore.ubports.com/app/loquiim.nfsprodriver) is a third party WhatsApp client for Firefox OS and Ubuntu Touch. Unfortunately the protocol and API the app uses will be deprecated next month, so the team needs help with the move to the new protocol. If you want to help with the move to the noise protocol, check out [their GitHub repo](https://github.com/loqui/im).

### Help UBports with marketing

If you want to join our marketing team, you can sign up [here](https://bit.ly/ubportsmarketingsignup).

## Now let's take some questions!

### Will UBports support Multirom?

No. We haven’t played with MultiROM in over a year and it would be too much work to fix it right now, so if you have MultiROM and you want Ubuntu Touch, you will have to choose one OS. That *may* change with Halium, but that’s not carved in stone yet and we won’t make any promises.

If someone in the community wants to maintain it, we will obviously support that, but we won't put any work into it ourselves.

### What's the future of X11-apps on Ubuntu Touch?

It's still possible to install desktop Linux apps on Ubuntu Touch using a Libertine container. It's not a very smooth experience, so we did not preinstall desktop apps in our images. If you're interested in playing with Libertine, you can [follow this guide](https://forums.ubports.com/topic/262/desktop-apps/2) a user wrote on our forum.

For 16.04, we definitely want to make installing X11 and Wayland apps simple and easy, but that's still looking to the future.

### What's the status of Mir on top of Wayland?

It depends on who you ask. If you ask a user, the platform is completely unusable. If you ask a developer, most of the stuff is already there. It [is all developed in public](https://github.com/ubports/mir/commit/a8cd1fcc1eb15c45297b2181fc93a3503aa69150), but it's in a very early stage of development.

### Why can't i just apt-get install something?

In fact, it is possible to use `apt` on the device if the filesystem is made writable. That's not recommended for most users since it's easy to break the system doing that. Unlike most desktop Linux distributions, we are using [image-based upgrades](https://wiki.ubuntu.com/ImageBasedUpgrades/) to update the system. That means that the [root-filesystem and all the packages are put together by us](https://wiki.ubports.com/wiki/How-a-UBports-Image-is-Built) and delivered to the device in one piece. This method allows for a lot faster updates than just running `sudo apt update && sudo apt upgrade` on the device, if you ever updated a Raspberry Pi, you know what we're talking about.

We are looking into making this process safe, easy and noob-friendly without taking away any hacker functionality in the future. \*cough\* Snappy \*cough\*.

### Have you thought about asking Canonical to ask the developers to move their apps to the OpenStore?

They would probably not do that. We already talked to a lot of developers and most actively maintained apps have been moved, so there's also not really a need for that. If you find an app in the Click Store that you would like to see in the OpenStore, try and get ahold of the developer yourself and ask them if they would be up to move their app themselves.

### How do I make an App?

App development on Ubuntu Touch is diffcult. The Ubuntu SDK is very broken and we are understaffed to fix it for the moment. Still there are some developers on the forum, that are always happy to help newbies solve problems. Also worth mentioning are [the app development guide](https://forums.ubports.com/topic/184/ubuntu-touch-programming-course) written by Mimecar,  [Clickable](https://wiki.ubports.com/wiki/Set-up-a-Clickable-working-environment-inside-an-LXC-container) from Brian Douglass and [the canonical documentation](https://docs.ubuntu.com/phone/en/).

Since most Apps are open source anyways, you can also try and take a look at their source code.

### What's the next patreon goal?

That kind of depends on what the community wants to see. We are thinking about additional financial support for Anbox and Halium, but that's yet to be decided. Feel free to share your feedback in the comment section.

### What's up with the Ubuntu Touch emulator?

The emulator has been broken for a while and it's not our highest priority to fix it at the moment. To fix it, our HAL would have to be ported to the Goldfish device, so it might make more sense to wait for Halium before fixing it. Maybe someone in the community wants to pick it up before then?

## That's it!

You still have questions that haven’t been answered yet? No problem, our next Q&A will happen on Saturday, June 10 at 6 PM UTC. If you won’t be able to catch us live, be sure to get your questions in beforehand in the comment section down below.

That’s it for this time, make sure to catch the next one. If you want to discuss this post, you can do that on the [UBports forums](https://forums.ubports.com) or in our [Telegram supergroup](https://ubports.com/telegram). There's also an IRC channel at #ubports on Freenode. Be sure to subscribe to our [E-Mail newsletter to stay posted on all things UBports](https://bit.ly/ubports)!

- Dalton, Jan and Andy


