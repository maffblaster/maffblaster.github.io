---
layout: post
title: Progress on Stage7
description: In this entry I just a brief update on Stage7 installer
date: 2014-12-04 12:13:25 -08:00
tags: "Digital Survival, Stage7, Gentoo Installer, POSIX"
---

This week I've been able to make some decent progress on the Stage7 installer. As of version 0.1.1-alpha there is now a check to determine if essential S7 "modules" (they are really more like classes) are missing. This new check does not extend the functionality of the code much for the end user, but it is a step in the right directly as far as the stability of the installer itself. Next I would like make sure the live medium contains the tools Stage7 needs. Most of them are generic GNU core utilities (echo, chmod, sort, etc.), but only a few "outside" tools exist exist as dependencies. Those are the important ones to check for. Before an ebuild for Stage7 is created it would be helpful to have the program to a self-check for required dependencies. After an ebuild is written the dependencies will simply be installed alongside Stage7 once it is emerged. The dependencies will not matter at all as long as people use Stage7 installer from a Digital Survival LiveCD/USB because all the required utilities will available. It will come in handy if other Gentoo-based distributions want to use Stage7; at least they can determine they are missing something.

I hope to push a few commits this weekend, and then focus more intensely on actually extending functionality to include Grub 2 and GPT support. God willing I'll be able to get those kinds of issues worked out rather quickly.

Onward and upward!

Maffblaster