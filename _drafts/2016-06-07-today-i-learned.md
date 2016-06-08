---
layout: post
title: Updating old Gentoo systems
description: Recently I inherited a Gentoo system that had not been updated for over a year. This article describes the route I took to get it up to speed.
date: 2016-02-24 12:17:00 -07:00
tags: "gentoo, updates"
---

Recently I inherited a Gentoo system that had not been updated for over a year (since <time>February 2015</time>). Gentoo, as a distribution, can have a particulatlly difficult time updating if there are long amounts of time between updates. This is a known issue and there is a Google SoC project to address calculating upgrade paths.

All that aside, what did I do to update this system?

It's pretty simple: I created a chroot from a stage3 tarball, then migrated the system into the chroot. This works simply when using filesystems such as btrfs.


