---
layout: post
title:  Modern Thoughts on Anti-Virus LiveCDs
description: Musings on modern virus tactics
date: 2014-12-04 12:13:25 -08:00
tags: "Digital Survival LiveCD, Stage7, Gentoo Installer, POSIX, Anti virus"
---

It seems to me that modern anti-virus programs running on live mediums (LiveCDs, etc.) will not be very effective these days, unless a copy on write (COW) file system is used. [There](http://wiki.dennyhalim.com/building-linux-livecd-with-antivirus) have been projects that have done it without COW type file systems.  These days viruses and malware have gotten tricky, and most anti-virus programs (I'm better versed with the Windows anti-virus programs) have done a good job keeping stride with the rapidly changing tactics.

While working on Microsoft systems at my place of employment come to be familiar the [BITS service](https://en.wikipedia.org/wiki/Background_Intelligent_Transfer_Service) that runs by default on every Windows machine since the XP operating system. Of course this service runs in the background (see here); but what it's doing is the interesting part. According to Wikipedia, BITS _"facilitates prioritized, throttled, and asynchronous transfer of files between machines using idle network bandwidth."_ The file that are transferred are software updates to various components of the Windows operating system. Components include Windows Update, Microsoft Update, Windows Server Update Services, Systems Management Server. BITS is also used by  Microsoft Security Essentials (aka Windows Defender _to fetch signature updates_ for MSE/Defender.

[http://www.dedoimedo.com/computers/linux-av-cd.html](http://www.dedoimedo.com/computers/linux-av-cd.html)