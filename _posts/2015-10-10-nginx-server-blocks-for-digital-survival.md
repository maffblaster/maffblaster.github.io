---
layout: post
title: Nginx server blocks for Digital Survival
description: An update on life.
date: 2015-11-15 13:23:18 -07:00
tags: "hosting, website, digitalsurvival, haroopad"
---

This week I upgrade my web services hosted on a personal server to run as [Server Blocks](https://www.nginx.com/resources/wiki/start/topics/examples/server_blocks/). It was much easier than I thought; just a a few lines added to the configuration file and then creating a review respective directories in <code>/etc/nginx/nginx.conf</code> and it was good to go!

> Note: “VirtualHost” is an Apache term. NGINX does not have Virtual hosts, it has “Server Blocks” that use the server_name and listen directives to bind to tcp sockets.

I'm really liking nginx as a server. It's fast and (so far) extremely easy to configure. Since the point of digital survival is to become as digitally self-sufficient as possible, I have been taking on the task of establishing and maintaining my own infrastructure. Things are currently not entirely where I'd like them to be...even this blog is (currently) hosted via the good graces of GitHub. It is simply a matter of time and effort to become digitally independent.

I have written this entry using [Haroopad](http://pad.haroopress.com/). [MarkPad](https://github.com/Code52/DownmarkerWPF) (formerly called Downmarker) was nice because it could dynamically generate a metadata document header for Jekyll sites, however it is largely unmaintained and seems to be heavier than it should be on system resources. Perhaps Haroopad will replace it as my default Windows markdown editor...

I plan on taking some time off my normal day job over Christmas break, which should give me some time to hack on [stager](https://github.com/gentoo/stager), the stage4 tarball installer for Gentoo-based operatings systems. It's been too long since. The project must go on. I have a feeling there are many users who will appreciate being able *quickly* to install a basic version of Gentoo.
