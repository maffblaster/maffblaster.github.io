---
layout: post
title: Today I learned mtab
description: mtab contains mount information
date: 2016-03-02 16:59:18 -07:00
tags: "til, today i learned"
---

Today I learned as a result of reading NeddySeagoon's reply on [this thread](https://forums.gentoo.org/viewtopic-t-813610-start-0.html) on the Gentoo forums, that <code>/etc/mtab</code> _is_ <code>/proc/mounts</code>.

If you chroot into a new stage tarball and run the <code>df</code> command there will be an error until either:

1. <code>/proc/mounts</code> are copied to <code>/etc/mtab</code> or
2. <code>/proc/mounts</code> are symlinked to <code>/etc/mtab</code>

The latter option is the better option since, as long as proc updates, it will keep the <code>mtab</code> file dynamic.

I also learned:

<quote>
If you install grub manually - not using grub install, then /etc/mtab is not consulted. 
The manual install is documented in the handbook
</quote>

I will start posting more 'Today I learned' entires, as they should be a helpful aid for me for look back on in the future.