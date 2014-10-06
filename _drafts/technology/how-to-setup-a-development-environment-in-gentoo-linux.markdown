---
layout: post
title: How to Setup a Linux Dev Box
description: How to configure a development environment in Gentoo Linux
date: 2014-09-24 14:16:50 -07:00
tags: "Setup Configure Software Engineering Development Developer Environment Gentoo Linux"
---

Configuring your Gentoo install to be a good development environment is pretty easy because the Gentoo system is *already* a development environment. However, there are a few generic things that can be done in order to establish your box as a *better* development box.

First, discover exactly what dependencies you will need for the software project your working on. You can typically find the dependencies with the software's documentation. If the software was written to be compiled on a Linux distribution that manages packages different than Portage, then you'll have to find the *equivalent* of the packages in Portage. It has been my experience that the Debian/Ubuntu package maintainers break up packages into smaller more specific packages. For example, dependencies for NixNote2 on Debian consisted of [list of amount of packages], but if you were going to build NN2 on Gentoo you only needed to install [list the packages]. If you're creating your own software then it's up to you to decide, which should be easy enough for you if you're building your own software.

Tools you can use for this step in the development process include
eix
emerge
equery

You can also use the web to determine the software you need. I found the site [packages.gentoo.org](http://packages.gentoo.org/) to be most helpful when trying to determine what packages were needed.

Second,

