---
date: '2008-05-02 17:14:10'
layout: post
status: publish
title: About that MacBook Pro 200 GB 7200 rpm Hard Disk
tags:
- Apple
- Performance
---

I've been working with this new MacBook Pro for about 2 months now.  I ordered the latest hardware refresh the day that it was released.  I'm very happy with it.  This new model replaced a 2-year old model which was also the "ultimate" configuration when it was out.  One of the things I noticed about the new MacBook was the much faster hard disk.  You can really notice the difference when you move to 7200 rpm from 5400 rpm.

However, as my recent tests indicate, you can find external disks that perform better than the internal 7200 rpm drive despite the fact that those drives are accessed over FireWire.  In particular, the LaCie BigDisk Extreme+ significantly outperforms the MacBook's internal drive when accessed via FireWire 800.

The reason?  The LaCie drive is a RAID 0 array.  [RAID 0](http://en.wikipedia.org/wiki/RAID_0#RAID_0), as you might recall, is striping with no redundancy.  Based on the size of the LaCie enclosure, I'd say there are two disks in there.  So the striping is writing part of the file on one disk and part of it on the other.  This is why this solution is perfect for my VMware guest file location.
