---
layout: post
title:  "Happy Holidays from UBPorts! (And FP2 fun!)"
date:   2016-11-22
description:	"We wanted to show a description here, but some idiot wrote it wrong."
---

Hello everyone!

We here at UBPorts hope that you're having/had an excellent set of holidays. As the year comes to a close, we'd like to thank all of our patrons, donors, and developers. You are what makes this project happen.

We've been busy around here, of course. Marius has returned for winter holiday at his school and my dashboard is looking busier than ever... an excellent sight when my name filled it up not too long ago.

We'd like to thank Smoose, a Netherlandic company specializing in open source software, for providing several Fairphone 2 smartphones to our developer community. Because of their generous donation, I have lots of news about the device.

The current daily builds for the Fairphone 2 have everything that you'll find on [the device page](https://devices.ubports.com/#/FP2) PLUS some basic GSM support. You are able to connect to a GSM network with SIM 1 at least (I don't have a second to test), send and receive SMS, and Marius reports that he has calling in a very experimental stage, though this may not be on system-image-server at the time of this writing. Mobile data doesn't work quite yet, but we're working on it.

To flash the development build, first note that it is not very stable and things break quite often. Now that that's out of the way, you'll need to first flash the recovery.img from [here](https://seafile.nigle.nl/d/62d505f0a7/),
Then run these commands:
```
adb shell mount -a
adb shell mount /cache
ubuntu-device-flash --server=http://system-image.ubports.com touch --channel=ubuntu-touch/devel_rc-proposed --device=FP2
```

As for other devices, we have a wonderful developer working on the Nexus 5 and its screen tearing problems in developer builds. It seems to be a bug between Mir and the Adreno drivers.

As always, if you'd like to support our project financially, you can donate toward a specific device at [https://devices.ubports.com](https://devices.ubports.com) or give a monthly donation at [https://www.patreon.com/ubports](https://devices.ubports.com). If you'd like to donate your time, check us out at #ubports on Freenode and we'll find something that you can do.

Again, happy holidays. And thank you. We're looking forward to a great 2017.

-Dalton (UniversalSuperBox)
