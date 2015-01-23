---
layout: post
title: GCC Compiler Options
description: In this entry I determined how to compile QT-Chooser
date: 2015-01-19 11:06:06 -08:00
tags: "QT5, QT-Chooser, GCC, -mtune vs -march, compiler options"
---

The QT-Chooser package on a system I use refused to compile for the [longest time](https://www.youtube.com/watch?v=a_XgQhMPeEQ). Checking the make.conf file I realized I had both -mtune=atom and -march=atom set for the CFLAGS variable which was causing problems with the package when I attempted to compile it. After changing -mtune to generic (-mtune=generic), I removed -march and emerged @world with only a few minor hiccups.

###-mtune vs. -march

What are these options and how to they effect things?

-mtune and -march are options that can be passed to the GCC compiler at run time in order to specific generate instructions for the machine's CPU.

-mtune "tunes the generated code for the specified cpu-type." mtune is magical because it has a "generic" option, which allows the system to compile code that can work on a verity of modern CPUs (IA32/AMD64/EM64T).

-march "allows GCC to generate code that may not run at all on processors other than the one indicated."

In summary use **-mtune=generic** if:
<ul>
<li>You want your compiled package to work on machines other than your machine;
<li>To choose a setting that doesn't break on any packages;
<li>an easy, no hassle solution.
</ul>

Use -march=<cpu-type> if:
<li>You have a specific CPU that code is compiled for;
<li>The smallest, fastest, lightest binaries are needed;


Both the flags can actually be used together. For the list of all available configuration options, and better explanations than I can provide, see GCC's [i386 and x86-64 Options](https://gcc.gnu.org/onlinedocs/gcc/i386-and-x86-64-Options.html#i386-and-x86-64-Options) page.

Maffblaster