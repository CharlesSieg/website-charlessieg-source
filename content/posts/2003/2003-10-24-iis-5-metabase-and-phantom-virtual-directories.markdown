---
date: '2003-10-24 10:00:00'
layout: post
slug: iis-5-metabase-and-phantom-virtual-directories
draft: false
title: IIS 5 Metabase and Phantom Virtual Directories
wordpress_id: '7'
tags:
- Tips and Tricks
---

I recently had a strange experience with IIS 5 and some phantom virtual directories. When I write "phantom virtual directories" I mean that IIS is handling requests for virtual directories that no longer exist. This is a description of the events leading up to this:  

  

One of the websites I was working with required two virtual directories, named genericdir and securedir. Both of these directories had their own web.config files. The both used an HttpFilter to handle requests for certain types of files. In fact, none of the requested files actually existed in the file system. When a request was received, it was parsed and a record retrieved from the database. The record contained BLOB data which was written out to the HttpResponse.  

  

In the latest version of this code, the need for these virtual directories was elminated by implementing an HttpModule on the parent directory and having it handle the URL parsing and BLOB writing. So we deleted the virtual directories.  

  

Where this gets weird is the staging environment we tested our code in. When a tested would click on a link to a file in genericdir, the server would respond with a server error in "GenericDir". This was weird because we had renamed all of the links and names of the virtual directory to the lowercase word "genericdir". The proper case version is what the old virtual directory used to be called.  

  

After much painful tracing and searching, I finally thought to do a backup of the IIS metabase. I opened the binary file in Notepad and found the following " G e n e r i c D i r" in the text. Obviously IIS still had a record of the virtual directory even though I had specifically deleted it and it no longer appeared in the IIS console. It was a phantom.  

  

This issue has not yet been resolved. There is a Microsoft KnowledgeBase article out there - 314938 - which describes how to manually remove offensive keys from the metabase but the script that is needed was removed from our staging servers during their security lockdowns. I will post again when I know more.  

  

**Update - October 29th, 2003**  

  

We finally resolved this issue. IIS did, in fact, still have records for these virtual directories in the metabase. We downloaded a tool from Microsoft called
[MetaEdit](http://support.microsoft.com/default.aspx?scid=kb;en-us;232068%22) which has a very useful Explorer-like GUI that shows all of the entries in the metabase. We found the "phantom" entries and deleted them. Problem solved!
