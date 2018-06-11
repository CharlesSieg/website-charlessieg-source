---
date: '2008-05-02 16:49:30'
layout: post
status: publish
title: Stunning Hard Disk Performance of LaCie BigDisk Extreme+
tags:
- Apple
- Performance
---

I as you can see [from an earlier post](http://www.charlessieg.com/?p=23), I am working on finding the best home for my VMware guest disk file on my MacBook Pro.  The LaCie BigDisk Extreme+ is looking like the best choice among hard disks but I wanted to know how the LaCie compares to the internal MacBook Pro drive.  I have the latest "ultimate" configuration which includes the 7200 rpm 200 GB drive.

This time around, I decided to use the industry-standard Mac benchmarking program [XBench](http://www.xbench.com/).  This is an excellent freeware utility that measures your Mac's performance in all of the critical areas: CPU, memory, disk, graphics card, etc.  I ran XBench against all of my disks in all configurations and the results, quite frankly, were stunning and unexpected.

You can view the full XBench results in this screenshot:

![XBench Disk Tests Capture](http://farm4.static.flickr.com/3004/2460607014_943199c97a_t.jpg)

XBench provides its results in a "score" which, for disks, is computed from the scores of the individual sequential and random disk access tests.

Again, the disks used are:



	
  * Internal MacBook drive: 200 GB at 7200 rpm

	
  * Seagate external drive: 120 GB at 5400 rpm over USB 2.0

	
  * LaCie BigDisk Extreme+: 1 TB at 7200 rpm over USB 2.0, FireWire 400, and FireWire 800


These are the results, rolled up to summaries of sequential and random for each disk:

	
  * Macintosh HD - Score: **40.64** (Sequential: 47.90, Random: 29.00)

	
  * Seagate over USB 2.0 - Score: **19.82** (Sequential: 25.78, Random: 16.09)

	
  * LaCie over USB 2.0 - Score: **37.28** (Sequential: 31.28, Random 46.13)

	
  * LaCie over FireWire 400 - Score **52.69** (Sequential: 54.06, Random: 51.38)

	
  * LaCie over FireWire 800 - Score **69.13** (Sequential: 92.88, Random 55.05)


Incredible.  As you can see, the LaCie external drive performed better in XBench disk tests using both FireWire 400 and FireWire 800:

	
  * Random access was almost twice as fast to the external LaCie drive over both FW 400 and FW 800 than the internal disk

	
  * Sequential access was slightly faster to the external LaCie drive over FW 400 than to the internal disk.  But, sequential access over FW 800 was almost twice as fast as to the internal disk.


Hands down, using a FireWire 800 drive that spins at 7200 rpm like the LaCie BigDisk Extreme+ is the way to go with VM guests.  Now...how to find such a drive in a portable format that runs off of the MacBook???

UPDATED:  [Found it!](http://www.charlessieg.com/?p=27)  And here is why [the LaCie is so fast](http://www.charlessieg.com/?p=26)!
