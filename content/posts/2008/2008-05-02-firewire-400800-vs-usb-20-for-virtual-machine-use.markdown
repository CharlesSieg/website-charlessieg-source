---
date: '2008-05-02 15:21:58'
layout: post
status: publish
title: FireWire 400/800 vs. USB 2.0 for Virtual Machine Use
tags:
- Apple
- VMware
---

I recently decided to switch to VMware on my Mac for hosting my Windows installation.  I started off with the VM disk image on my MacBook hard disk.  I have a MacBook Pro with a 7200 rpm 200 GB hard disk.  The performance of the VM was not ideal.  Obviously there is disk contention between Mac OS and VWware.  But I hesitated to move the file over to an external drive because I didn't feel an external disk would perform any better.  But I went ahead and put it to the test.

For my testing purposes, I am using two different external hard disks that I have.  My portable hard disk is a [120 GB Seagate drive spinning at 5400 rpm with an 8 MB cache](http://www.amazon.com/Seagate-Portable-External-Drive-ST9120801U2-RK/dp/B000F8GX1W/ref=pd_bbs_11?ie=UTF8&s=electronics&qid=1209764395&sr=8-11).  My desktop hard disk - mostly used for backups - is a [1 TB LaCie BigDisk Extreme+ in a built-in RAID 0 configuration spinning at 7200 rpm with a 32 MB cache](http://www.lacie.com/products/product.htm?pid=10923).  The Seagate has only a USB connection but the LaCie has USB, FireWire 400, and FireWire 800 connections.  I tested them all.

For the tests, I copied a 3.31 GB file (a big, fat Visual Studio ISO) from the MacBook to the external drive.  So this test demonstrates performance of write operations to the external disk.  The results for writing are:



	
  * 2:22 for copying the file to Seagate over USB 2.0

	
  * 2:11 for copying same to LaCie over USB 2.0

	
  * 1:35 for copying same to LaCie over FW 400

	
  * 1:09 for copying same to LaCie over FW 800


We can draw the following conclusions from this data:

	
  * The 7200 rpm drive is about 8% faster than the 5400 rpm drive when copying over USB.  But part of this may be because of the significant (10x) difference in disk size.

	
  * FireWire 400 is about 38% faster than USB for the same disk.

	
  * FireWire 800 is about 38% faster than FireWire 400, and almost 90% faster than USB on the same drive.


The precise size of the file is 3,554,287,616 bytes on disk (not sure exactly why it rounds to 3.31 GB).  So if we take the fastest time of 69 seconds and divide the file size by the time, we get a transfer rate of 51,511,414.7 bytes per second.  Converting this into MB/s with 1,048,576 bytes per megabyte, we get approximately 49.125 MB/s sustained transfer rate.  The LaCie website indicates that the sustained transfer rate is between 40 and 50 MB/s.  This test shows that the LaCie is performing very close to high end of this range.

But I still need to determine how the LaCie compares to the internal MacBook Pro 7200 rpm drive.  More on that in the next post.  For now, we can conclude that if you are going to run a VMware guest from an external drive, definitely run it on 7200 rpm FireWire 800.
