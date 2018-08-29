---
date: '2005-09-21 12:42:00'
layout: post
slug: comments-back-online
draft: false
title: Comments Back Online
wordpress_id: '395'
---

I think I have finally worked out the comments functionality in the Narrative CMS. As originally posted [here](http://www.forkbender.com/content/70d986fd914e41fb8352496430a025cb.htm), I have, in past months, had a lot of problems with comment spam. Unscrupulous marketers send out spambots which crawl my website, leaving advertisement comments on every page that accepts comments. To end this, I implemented a captcha system which defeats spambots by requiring a security code before submitting comments. The security code is displayed as an image on the page and all the user has to do to submit a comment is to type in the code in the image. Easy for people to do, hard for spambots to do. This solved the comment spam problem. However, in recent months I migrated Narrative to a on-demand build model. This means that the content on this website is static and is only refreshed when content is added, deleted, or changed. When a comment is submitted, it is displayed on the page with the article that the comment is about. This is a kind of indirect change to the content. So I needed a mechanism for Narrative to accept comments, save them into the database, and then automatically rebuild the originating article page. Additionally, certain other pages - such as the home page - need to be rebuilt also to show that comments are now present. Without getting into the technical challenges, the end solution is a combination of AJAX and server-side modules working together. Now when you post a comment, your comment is saved and the page is rebuilt and refreshed in your browser instantly. Let me know what you think.

