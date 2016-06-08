---
layout: post
title: Today I learned insmod
description: modprobe is a better insmod
date: 2016-03-04 9:59:18 -07:00
tags: "til, today i learned"
---

Today I learned that <code>modprobe</code> is essentially a smarter version of <code>insmod</code>. I knew of insmod previously, but I had no idea why the younger utitity (modprobe) was created.

modprobe improves upon insmod by adding version and dependancy checking so that the kernel doesn't immediately inhale any module thrown at it. With modprobe, it will make a better choice when considering what it needs in order for a kernel module to work as indended.