---
layout: post
title: Cloning a MediaWiki with Git
description: In this entry I discuss my attempt to use the Gentoo wiki without an internet connection.
date: 2015-02-10 11:46:30 -08:00
tags: "Git, MediaWiki clone, Backups, Redundancy, DigitalSurvival, Digital Survival, Survivalist"
---

Last week [I purposed a suggestion](https://wiki.gentoo.org/wiki/Gentoo_Wiki:Suggestions#Make_the_Wiki_downloadable) to create a data dump for the Gentoo wiki. It would not need to be exactly like Wikipedia; I was hoping for at least a quarterly dump. The maintainer of the of Gentoo wiki said there would be too many problems creating a dump because they "have enough problems as is with stale documentation and zombie clones of long-gone Community wikis." I understand his concern, however it doesn't solve my problem have having an offline copy of the wiki in the case I lose internet access.

[Pavlix](https://wiki.gentoo.org/wiki/User:Pavlix), another Gentoo wiki user, suggested the possibility of downloading the wiki's files via a Perl module for git so I started on the project. I'll post another entry when I successfully have cloned the wiki locally. Eventually I'd like to create an ebuild for the wiki's files, host it in an overlay. This way other users who wish I have a copy of the wiki locally can do so.

