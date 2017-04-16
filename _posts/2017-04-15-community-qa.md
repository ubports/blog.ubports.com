---
layout: post
title:  "UBports Community Q&A: April 15, 2017"
date:   2017-04-15
description: "Questions, Answers, and more Questions."
categories: 
---

![supercoolquestions]({{ site.url }}/assets/2017/04/15-marius.png)

Today marked another Q&A session in the books. You can find it right over [here](https://www.youtube.com/watch?v=gNKxMiAnO1I) on our shiny new Youtube channel! The following are the majority of asked questions and a summary of their answers.

If you'd like to discuss, you can come to [our Telegram group](https://ubports.com/telegram), the [forums](https://forums.ubports.com), or you can post a comment using the below Disqus embed.

Thank you all for your support! Without further ado, here's the summary!

Will you support old official devices?
--------------------------------------
Yes. All devices but the Pro 5 and M10 will be in "legacy" mode, getting critical bugfixes and security updates. These will be in-between due to their closed Android source tree.
We have mirrored the system-image-server so we can host the old images at some point.

How will the official devices be updated?
-----------------------------------------
They will probably require a reflash.

Which device should I buy?
--------------------------
You should probably buy one of the stable devices: Nexus 5, Fairphone 2, or Oneplus One.

When will there be new ports?
-----------------------------
Once we have the infrastructure in place to service new devices.

What happens to the core apps?
------------------------------
We're moving them to GitHub. After our build infrastructure works, we'll work on them.

What will you do with the Ubuntu store?
---------------------------------------
We're forking the OpenStore at openstore.ubports.com. We will ask app developers if they would like to place their apps on this store. Otherwise we cannot move the apps. They can be forked and placed on our new 

What will you do with Ubuntu One services and push notifications?
-----------------------------------------------------------------
We might use Ubuntu One sign-in services. Push notifications are going to be handled by applications rather than our servers. We don't want that data.

What does the future hold for the SDK?
--------------------------------------
Making a decision on that is on our todo list.

Do we still want to make Mir run on top of Wayland, if Canonical is going to keep working on Mir?
-------------------------------------------------------------------------------------------------
Canonical is still maintaining Mir for IoT applications like digital signage. We expect that this means that the desktop and mobile focus will be lost. We still want to run Mir on top of Wayland to give ourselves and Yunit more options in the future.

What is the plan for sync services?
-----------------------------------
We would love to have sync services, but we need to have more boxes checked before we can worry about that part.

Does Anbox fit into your plans?
-------------------------------
You bet! Anbox works on the Oneplus One already, it will come to devices that can support it.

Will Anbox send notifications through the Ubuntu system?
--------------------------------------------------------
We have a lot we need to fix related to the system and notifications. It's something we would like to tackle but this is a long term fix, it wont be in the short term.

Will you ship the Google Play Services with Anbox?
--------------------------------------------------
No, we are not legally allowed to do that.



