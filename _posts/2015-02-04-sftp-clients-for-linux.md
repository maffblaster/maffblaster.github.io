---
layout: post
title: SFTP Clients for Linux
description: Documentation on a trick for people who might now know about SFTP in Linux.
date: 2015-02-04 08:56:14 -08:00
tags: "SFTP, Linux, WinSCP"
---

Until someone can show me a more powerful open source tool tool, the most powerful SCP/SFTP related tool for Windows is definitely WinSCP. Having a wonderful GUI and savable sessions it puts Putty's SCP (psftp.exe) to shame. It makes transferring files between Windows and Linux a breeze.

Tools like WinSCP are important to have available on Windows because Windows' file manager (Explorer) does not make it easy to connect to other operating system's drives over the network. Explorer is great for connecting Windows-to-Windows shares, but not great for anything Linux or Mac related. Most users setup a Samba share using at Linux system to avoid networking related problems. Windows plays nice because Samba emulates the way Windows-to-Windows file sharing works.

When working with Linux-to-Linux systems, it first appeared to me that were only a few installable SCP transfer tools for working between Linux systems. As I continued to investigate I was reminded to be thinking in the right categories about how Linux works. In the Linux world file managers integrate encrypted support for connecting to other drives in directly into the file managers. Dolphin (KDE), Nautilus (Gnome), and PCManFM (LXDE) all have support for SFTP built in.

Lesson learned: use the built in file mangers features for efficiency!

That's all for now.

Maffblaster