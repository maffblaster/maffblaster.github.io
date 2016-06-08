---
layout: post
title: How to setup an EFI capable QEMU virtual machine in Gentoo
description: In this entry I illustrate how to setup a QEMU virtual machine in Gentoo.
date: 2015-02-11 15:18:16 -08:00
tags: "EFI, vm, virtual machine, QEMU, Gentoo, Release Engineering"
---

For QEMU to support EFI booting special EFI firmware needs to be used. This special EFI firmware was created by Intel and is known as OVMF.

[http://www.tianocore.org/ovmf/](http://www.tianocore.org/ovmf/)

There is an official wiki available, but as of right now it doesn't contain a ton of useful information: [https://github.com/tianocore/tianocore.github.io/wiki/start-using-UEFI](https://github.com/tianocore/tianocore.github.io/wiki/start-using-UEFI)

The main thing users need to be aware of when configuring QEMU to have EFI support is the -pflash option.