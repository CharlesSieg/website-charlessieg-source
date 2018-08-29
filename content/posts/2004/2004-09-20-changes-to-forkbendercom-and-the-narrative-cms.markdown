---
date: '2004-09-20 15:15:00'
layout: post
slug: changes-to-forkbendercom-and-the-narrative-cms
draft: false
title: Changes to ForkBender.com and the Narrative CMS
wordpress_id: '170'
---

There have been some changes to ForkBender.com recently. These are due to me getting closer and closer to the 1.0 release of the Narrative CMS and finalizing some design decisions.  

  

There are a number of small issues with the website which I am working through right now. Some have been very challenging to debug but I fully expect all issues to be resolved soon. One of the big changes you may notice is that all pages have an HTM extension now. This website is no longer an ASP.NET website in the normal sense of the word. Rather, the website is more like Vignette in that it generates the HTM page in response to a system request. Further requests for the same content get the HTM file off of the file system rather than dynamically regenerating the same page. The dynamic capability is still there with Narrative but I added this content caching ability to take advantage of kernel mode caching in IIS 6 - something ASP.NET cannot do.  

  

Because of this change, comments posted will not immediately be visible on the article page. Rather, the comments will be shown when I regenerate the page. This is good for me, actually, as it gives me an opportunity to screen comments before regenerating the page.  

  

Feel free to leave comments if you wish.

