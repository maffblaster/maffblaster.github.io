---
layout: post
title: The Power of Gentoo Linux on a MacBook Pro
description: Here is where I prove to you that Linux is powerful and should be used as your primary OS.
date: 2014-09-21 23:58:37 -07:00
tags: "13 inch Mid 2010 MacBook Pro Install Gentoo Linux Custom OS"
---

I'm continually impressed by free and open source software. Linux is about five times friendlier to old hardware than Windows 7 or Mac's OSX Mavericks. Well, before I dig in, I should probably start with the back story...

In the summer of 2010, before she started attending Moody Bible Institute - Spokane, my wife purchased her first computer. It was a 13 inch Mid 2010 MacBook Pro (Apple's naming scheme, not mine). This computer worked well for her; she mainly used it for web browsing, e-mail, and working on homework assignments during her time of study. After we started dating I became responsible for maintaining her computer. "Maintaining" Apple products that use Apple's operating systems primarily consists of installing updates. If you're doing more than installing updates you're probably not doing something right. That's what Apple expects of people and it's exactly what they want.

As the years of knowing my wife progressed and I continued to install updates she noticed her computer ran slower and slower. The slowing was partly due to the nature of updates on binary-based distributions, but it was also due to the minimal system requirements of day-to-day web browsing. From 2010 to 2014 many websites morphed into full-scale JavaScript applications in themselves, especially the three primary sites she visited (Gmail, Facebook, YouTube; *especially* Facebook).

About two or three months ago, we're talking June or July 2014, I learned that OSX Mavericks, which was the newest version of OSX available at the time, was released as a free update through the App Store. Like many other individuals I decided to get it. Unfortunately it was the straw that broke the camel's back. The little 2.4 Ghz Core2Duo and 4 GBs of RAM couldn't handle it. Firefox could not play HD (720p) video on YouTube without dropping to *very* low frame rates. Nor could my wife have more than five tabs open while she did other work on her system. Using her computer became a chore, which I could not bare to witness. The universal standard for effective computer use is this: if you're able to work faster than your machine when doing basic tasks, then something needs to change. Either you need:

1) A completely new machine. Not a bad option, but tends to be the priciest. 

2) Upgrade the hardware in your current machine. Pretty simple if you simply need more RAM or a faster hard drive. Decently inexpensive.

3) You need to figure out how to get the most out of your current machine. *Always* the cheapest option if you know what you're doing.

As you observed, the options above are listed in order of most expensive to least expensive. I ended up choosing a combination of option 2 and option 3 because I didn't want my wife to continue using a 5,400 RMP hard drive for the rest of her time using her current setup. Not that older hard drives aren't useful; I simply made the choice the drive was a bit too slow for her daily use.

My first plan of attack was to purchase a flashy new solid state hard drive and use the OSX install disk that came with the Mac to reinstall the operating system, but that plan failed. It turned out that OSX recovery disk did not have the proper driver for the new SSD. It was to be expected since SSDs were not as popular in years previous to 2010, which is when the disk was created. I made commitment in my mind that if OSX couldn't install on my first try I would attempt to install Gentoo as the primary OS on the MacBook hardware.

I then turned to my trusty SysRescCD, which is literally my favorite Linux distribution. I use it because it is currently one of the only distros with a ISO that supports EFI boot. Regardless of what you might think of it EFI is the future, so her MacBook had to be EFI bootable. It was actually very easy to add an EFI boot entry to the MacBook's EFI firmware. By the way, some people will refer to the EFI firmware as "BIOS." I've even seen actual EFI firmware refer to itself as "BIOS," which was simply not true. You either have EFI firmware or you have BIOS. You can't have both at the same time in the same way. That's simply applying the law of non-contradiction. There *is* something to be said for EFI firmware that has BIOS compatibility built in, however the firmware itself is still EFI firmware, not BIOS firmware. I digress.

After a few hours I had a basic, but happy, Gentoo install. There was still many things left on the system to configure, but at least my wife could use her system. Generally when I install a fresh Gentoo operating system it takes me a while to work out the kinks and get everything working as it would naively in Windows, or in this case OSX. I realized during this most recent Gentoo install that I needed a way to install Gentoo automatically so that I could be working on other projects during the install and only spend time on the things that are difficult to configure. You can learn more about my efforts to do so by looking at [this project](https://github.com/DigitalSurvival/Stage7).

This evening I was working out a few of the kinks that happened as a result of the Linux switch. There were a few areas that have not been worked out yet. The webcam and the media control keys are not working, but I haven't done much to figure out why. At least that gives me an opportunity to return to this entry and make some changes/updates. If you're interesting in finding more information, including many helpful configuration files and how-to instructions by checking out [the repository I created](https://github.com/Maffblaster/Mid-2010-MacBook-Pro).

Relative links:

[The Official Gentoo Wiki's Mid 2010 MacBook Pro Retina article.](https://wiki.gentoo.org/wiki/Apple_Macbook_Pro_Retina) This article is actually for a newer MacBook than the one I used, still helpful information.

[Gentoo Linux on Apple MacBook Pro Core2Duo](http://www.odi.ch/prog/macbookpro/index.php#18) guide. This was the best guide that I found.

I will probably write my own guide and link to it here eventually. :)

Toodles,

Maffblaster