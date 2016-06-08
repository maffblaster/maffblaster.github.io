---
layout: post
title: A Secure Distributed Update System for Gentoo
description: In this entry I discuss 
date: 2015-03-17 16:45:26 -07:00
tags: "Gentoo Linux, Portage, Survival, Distributed, Appropriate technology"
---

This entry is simply a musing, of sorts. Not all my ideas have been worked out. I simply wanted to write down some of the ideas that I have been pondering for the past few hours.

### Making Binary Package Support more Accessible to Portage users on LANs

Recently I have been doing some reading on Wikipedia regarding different philosophies behind technology. I found the [Appropriate technology](https://en.wikipedia.org/wiki/Appropriate_technology) article to be one of the most interesting articles on the wiki. The appropriate technology philosophy is actually the reason I started one of my [side projects](http://www.digitalsurvival.us) (do not be expecting much work to be done so far via Digital Survival; it has been a back burner project for a while).

The greatest strength of Gentoo is it's heart: Portage. Portage makes it possible to do many neat things. There is already binary package support built into Portage. If there is a binary host machine running on the network all that is needed is to point Portage to the network path and boom! Access to installing binary packages has been granted! This method, however, is not secure by default. Someone could try to redirect a machine's request for a binary package from a specific server to a compromised machine.

One way around this is to use SSHFS with public/private key pairs. The local machine could, at boot time, mount a read only network directory over SSHFS. The machine could then pull pre-compile binary packages from the network location to install locally. For this approach, all that is needed is FUSE support built into the kernel and a placing of the public key on the host file system.

But is there a better method? A better approach?

What if Portage had an option that could handle this automatically?

###The Ultimate Binary Host Machine

What if, using the power of Portage, binary host machines could be placed on a LAN. Client machines could easily, and automatically, find secure binary host machines and ask for specific binary packages?

The host machine would need a lot of space for this to work properly, but what if a binary host machine would build every package available with every variation of USE flags set, then use BTRFS deduplication powers to create binary diffs of each variation of the packages (potentially saving lots and lots of space). This way every way to build the package would be available on the binary host. No matter which way the client asks for 

Potential problems:

Compression would significantly reduce the number of possible dedups. One bit (literally, a bit) of difference would change the file, making it appear to be entirely different.

###Trust built into Discc

The way things are now, it is possible to have a trusted machine running Distcc.

Unanswered questions

How would a distributed update system work?