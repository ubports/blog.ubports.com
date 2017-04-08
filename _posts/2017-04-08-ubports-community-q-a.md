---
layout: post
title:  "UBports Community Q&A: April 8, 2017"
date:   2017-04-08
description: "Someday we will implement these and my previous ones will confuse a lot of people."
categories: 
---


On Friday, April 7th, 2017, we started what will be a long journey into the future. A core team meeting at 1800 UTC was quickly followed by a community Q&A. The Q&A is public for anyone to view. You can view it [here](https://www.youtube.com/watch?v=MVEm4X2ptEk) or continue reading for a list of the Q's and A's. Remember that as this is still an early time for our project, almost everything here is subject to change.

### Two crashes and we finally arrived at Hangouts on Air.

After crashing both jitsi.org and talky.io, yesterday's UBports Q&A started with Mariogrip summing up what happened so far:

Our short-term plan is to keep Unity 8 and Mir as is. We need to learn how to build these projects into system-image-server through automated means. We will also look into running Mir on top of Wayland as a stop-gap during the Yunit (unity8org) transition to qtWayland (if that happens, their community hasn't decided yet).

We DO NOT want to be maintaining a display server. By moving to Wayland we get native Libhybris support, meaning we should be able to work directly on the upstream libhybris. Until that is possible, though, we will ensure that our infrastructure can support our OS: We need better updates and some release policy changes: devel (nightly), rc-proposed (weekly), and stable (manual push), details TBD.

We plan to support existing devices, but they'll be in "legacy mode" due to hardware limitations. They'll get small updates and bugfixes on the current 15.04 base, but will probably not make the jump to 16.04. UBports will also not provide Android base updates, though we haven't planned these for our current stable devices either.

### The Q&A

####  Q: What about the bq M10?

A: Because this device is more powerful and still very usable, we'll probably make it an "official" device rather than a "legacy" one. This means that it will get whatever new OS we build.

####  Q: What about the Unity 8 desktop experience?

A: We need a desktop experience since that's the important part of convergence. We won't develop more on Mir, but Unity 8 must be maintained for the important convergence goal.

####  Q: How can I help if I want to do QA or testing?

A: Right now we have a Google Form that will lead you through all the testing steps, but we need a better solution. More documentation needed. Just using your device and reporting bugs that you find is a very good solution.

####  Q: What will happen to the notification servers and the Ubuntu One dependant services?

A: We can continue to use OpenID through Canonical (Ubuntu One), but we'll remove the server components from the OS since we want to redefine the notification service. The notification service is FAR too closed for our liking right now. We're going to focus on usability rather than confinement since we're breaking the current security model anyway. Using old Android kernels is the worst security flaw we have and there's no way we're going to make that go away soon.

####  Q: Wait, so confinement is going away?

A: No, but we're going to make the system more open and usable rather than locked down.

####  Q: Why aren't we collaborating with [Yunit](https://yunit.io)?

A: We are having conversations with them. They want more desktop focus while we have more mobile focus. Both projects benefit from the other's work. Having two forks of Unity 8 makes no sense.

####  Q: Will we collaborate with Mer or Plasma Mobile?

A: It's still on the table. It makes sense for all of us to work together on a common Android base and build our own distributions on top of that. Our communities could all work together and a single device enablement would open it up to lots of new OS's. Working together means more success for all of us.

####  Q: You've split UBports contributors into teams. What's the goal of this?

A: A more structured project means that we all have a say and all have a defined purpose. Having different teams means that a team can make a decision faster than if we needed every contributor to agree. We also split into multiple group chats so we can actually talk to each other without being buried.
We have the infrastructure, developer, communication, and QA teams. We're looking at adding more. Also, the communication team is the best team and no one can say otherwise.

####  Q: Will the Open Store continue?

A: TODO. We're going to either fork the store or maintain it since it's shutting down.

####  Q: How will you finance all of this?

A: [Donations](https://ubports.com/get-involved). One-time Paypal donations and Patreon contributions are what will keep us going. Servers are going to be extremely expensive, devices aren't getting cheaper either. Each member of the QA team will need most of our devices to test. We're not worrying yet, but this will become a problem in the near future.

####  Q: Can we hire full-time people?

A: It's in the future, but we would *love* to. It would make the project move much faster. A developer and a sysadmin allowing the developers to focus only on developing would be perfect. We don't have the money for that yet. Or the legal knowledge.

####  Q: Will we sell devices pre-installed with your OS?

A: That's tricky. Legal issues like Qualcomm licensing would absolutely kill that business... unless we ship the device without modifying any of the proprietary blobs. Long story short, that's out of our scope right now.

####  Q: What happened to the Station Dock?

A: It still exists. It's been postponed for an indefinite amount of time. It's based on a Raspberry Pi so we might just release the firmware and call it a day... 
inb4 a Chinese company takes the software and ships it as closed-source, making a lot of money.

####  Q: Are we following Canonical's plan or making our own OS?

A: We're following for now, but we may change direction quickly as we determine what went right and wrong with Ubuntu Touch.

####  Q: Will we make Sailfish OS apps compatible with your stuff?

A: Maybe? We'll have very different design languages.

####  Q: Will we support snaps?

A: Yes, but legacy devices might not. We don't think we'll do the atomic system updates (Ubuntu Core), only apps. We have no idea how atomic updates would work with the Android ecosystem... our guess is that they probably wouldn't.

####  Q: Will we fix long-standing critical bugs in Ubuntu Touch?

A: We'll try to polish the OS as much as we can, But don't expect OTA-16 anytime soon.

####  Q: Will this be hard without Canonical?

A: Yes and no. Since this has now become a community project, we've seen a lot less pushback and a lot of people stepping up to help. When Canonical was the only one developing Unity, people hated it. Now people are coming out of the woodwork to say that they loved where it was going and will miss it. We have seen around 400 new devices hitting our system image server since the news. There's a strange effect that Canonical has on the Open Source community.

####  Q: Will there be a guide for porting Ubuntu Touch on the UBports website?

A: You bet.

####  Q: But how do we really ***feel*** about Unity and Touch being dropped?

A: We understand that the project wasn't making money and that Canonical as a company should make money. We really can't argue with the decision and Canonical has given us no reason to harbor any ill will (We got to present at MWC! How cool is that!?).

####  Q: Will we be using stuff from Firefox OS?

A: We stole some of their AGPS stuff, if that counts.

####  Q: Will we keep the name?

A: Hard to say. No reason to change it yet, but once we further separate ourselves from Canonical we'll probably change it.

####  Q: Will we continue the core apps?

A: Yes, but in a feature freeze state unless the community is very willing to help. We need to sort out the bottom of the stack before we work on the top.

####  Q: Can we mirror the core apps to GitHub (and use Git rather than Bazaar)?

A: Sure. Code hosting at GitHub is a bit more accessible than Launchpad so we totally understand where this question came from.

####  Q: Will we keep using Launchpad?

A: Yes. The project management of Launchpad is more than a Kanban board. We like the bugs.launchpad.net more than Github's issue tracker, for example.

####  Q: Will we consider moving to GitLab?

A: If we wanted to use it for Git only, sure. But we don't. So no. GitHub is simply a more accessible platform.

####  Q: Are we coming to [Ubucon Europe](https://ubucon.paris)?

A: YES! We're going to be showing off all of our work that hasn't happened yet! Go future us! WOOOOOH!

####  Q: Snap only supports kernel 3.10 and above. How will you support older phones?

A: Backports and patches. Canonical has already started on this. (Dalton's note: Snaps work on kernel 3.4 with a namespacing patch, they just don't have confinement). Any newer devices that we port to will have kernel 3.10 or above anyway, so we're not that concerned. We have a LOT to handle before we even consider this problem.

#### Q: Are there more updates coming to the current UBports devices?

A: Yes. We are still focusing on our efforts to bring our stable devices to a good state with the Canonical Ubuntu Touch images. We've set the Stable release target for April 30th, but we might not hit that any more.

#### Q: What if I missed the Q&A but I want to talk to / yell at you?

A: You can get a hold of us in [our Telegram supergroup](https://ubports.com/telegram). We also have a neat little Disqus embed that you can use on all of our blog posts! We'll be holding more of these community Q&A's in the future. Our next one should be in about two or three weeks, stay tuned!

-Dalton and Jan
