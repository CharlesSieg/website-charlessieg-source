---
date: '2005-06-22 17:41:00'
layout: post
slug: june-2005-edition-of-narrative-cms
status: publish
title: June 2005 Edition of Narrative CMS
wordpress_id: '134'
tags:
- Narrative
---

It's been at least 3 or 4 months since I got a new release of the Narrative CMS out there. I'm in the progress of updating it now and am still working out a few glitches.

This version solves two major issues that previous versions have had. One is related to comment spam. This website gets *a lot* of comment spam. You don't see it because I clean it up but I've gotten at least 10,000 spam comments from spam bots out there. It's a real pain. To solve this, I created a captcha system in this release. I haven't turned it on yet but will soon. You've all seen it before - a little image comes up with some numbers or a word in it. You, the human, have to read the number and type it into one of the boxes in the comment form. When you submit your comment, the CMS determines whether the number you typed matches the one in the image. If it doesn't match, the CMS assumes you are a bot and does not post your comment. Sorry if this is an annoying extra step in leaving a comment but it saves me a lot of time

The other issue that is solved by this version is something you will never notice. It has to do with automatically rebuilding the pages of this website when content in the website changes. Narrative has a comprehensive class library so dynamic pages are very easy to do. But most weblogs, like this one, don't need to be completely dynamic. As you've seen recently, the content does not change every 5 minutes. It might change once or twice a day. So there is no need to put the extra load on the server to dynamically rebuild the page every time someone views it. Instead, the CMS now rebuilds various pages of the website as needed, when content is changed, or when the template used to build the page has changed. It's pretty cool for me and other content authors using Narrative but the end-user will never know any difference.

In this version I am also able to finally release my custom tagging assemblies. The tagging assemblies are code libraries which are used in the page building process to replace template tags with content. ASP.NET is not used at all to build the pages of this website. Rather, a template is loaded into a parser. The template is parsed. When tags are identified, the parser offers the tag to each tagging assembly. If a tagging assembly recognizes the tag, the assembly can take the tag, run some code, and replace the tag with something meaningful. I may give some examples of this later but, suffice it to say, it makes maintaining and expanding this site vastly easier than before. In fact, I can create a new weblog in less than a minute in Narrative. Powerful stuff.
