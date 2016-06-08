---
layout: post
title: How to Install Gentoo on a Lenovo ThinkPad W530
description: In this entry I talk through the install process for Gentoo Linux.
date: 2014-09-22 14:13:51 -07:00
tags: "ThinkPad W530 Gentoo Linux Install Custom OS"
---

**UPDATE:** I adapted a version of this install guide for [an article on the official Gentoo Wiki](https://wiki.gentoo.org/wiki/Lenovo_Thinkpad_W530), now everyone can add what they discover to be useful in their own experience to the Wiki article.

If you were searching the internet for information on how to do what is in the title of this article, I hope you find this entry to be most helpful. 

This entry has been written  to a very small portion of the world's population. Seriously, how many people actually purchased a W530? Probably less than 250,000 W530s were produced...still I believe it will be helpful for some. Lets get started!

## Prepare ##

Adequate preparation should be established for the case something should go wrong in the middle of installing Gentoo. The following list does not only apply to the current hardware set in this article; it applies to whenever attempting to install Linux on any machine:

* **Backups** - If the computer owner finds any value in being able to restore the factory existing operating system, make sure appropriate measures are taken to create a full system restoration. This is a nice fall back option in the case something goes wrong while installing Linux.
* **Time** - Allot enough time for installing Gentoo. The length of the install process varies. Experienced Gentoo users are mostly limited by the speed of their current hardware where beginners are limited by the Gentoo learning curve.
* **Diligence** -  Dedication is required in order to configure all parts of the hardware to work properly. Unfortunately most manufacturers do not deliver open source drivers for their hardware. Linux users go through great lengths in order to build or find open source drivers that are compatible with their hardware.

## Kernel ##
For basic Intel graphics with the potential to utilize the Nvidia card later on, these kernel options should be set:
<pre>
Device drivers -->
   Graphics support -->
      Direct Rendering Manager -->
         <*> Intel 8xx/9xx/G3x/G4x/HD Graphics
          [*] Enable modesetting on intel by default
</pre>