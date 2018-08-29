---
date: '2003-10-03 19:04:00'
layout: post
slug: manually-removing-a-vignette-installation
draft: false
title: Manually Removing a Vignette Installation
wordpress_id: '11'
tags:
- Tips and Tricks
---

In the event that one or more CDS or OMS machines are installed and the CMS has been removed, going into Add / Remove Programs and uninstalling Vignette will fail with a message that Vignette must be “unconfigured” first. Unfortunately, without the CMS running, nothing can be removed in the Platform Manager and so the whole installation must be removed manually.

1. Stop all services and then set them to Disabled. Depending on what you have installed, there may or not be any services to disable. Reboot the machine after disabling the services.

2. In the C:\Vignette directory there is a file called insts.cfg. Delete this file.

3. Go to Add / Remove Programs again and uninstall Vignette. This will remove all the Vignette binaries, etc. but will leave the Vignette directory.

4. Delete the Vignette directory. Ignore the warning dialog that appears.

5. Reboot the machine. The removal is complete. Any docroot directories, etc.
remaining in the Inetpub directory or other locations remain to be removed with discretion.
