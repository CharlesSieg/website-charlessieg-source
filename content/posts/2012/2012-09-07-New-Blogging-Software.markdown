---
layout: post
title: "New Blogging Software"
date: 2012-09-07 10:21
comments: false
tags: 
published: true
---

I recently moved my blog from the [WordPress](http://www.wordpress.org) engine to [Octopress](http://octopress.org).  The page you are reading now is a static HTML page which was rendered by Octopress on my computer and then published to a [Linode](http://www.linode.com) server.

<!--more-->

### Problems with WordPress

When it was running, my WordPress installation was hosted in the [Rackspace Cloud](http://www.rackspace.com/cloud/public/sites/).  I was initially very happy with it - mainly for the ability to easily apply new style templates and add functionality with plugins - but eventually stopped using it for a number of reasons:

1. I used [Markdown](http://daringfireball.net/projects/markdown/) for writing all of my posts.  I will probably write more about my reasoning for this in a separate post, suffice it to say that Markdown is cleaner than HTML yet results in standards-compliant HTML output.
2. I got tired of keeping WordPress up-to-date with all of the security patches, etc.  While I was on WordPress, both this website and my company websites were hacked from time to time due to vulnerabilities in WordPress.
3. Given my preference for writing in Markdown, I typically do my writing in an editor which understands Markdown and can provide an easy preview of the rendered post in HTML.
3.  I didn't really like having all of my content stuck inside of a MySQL database on some server somewhere.  I prefer plain text files, stored locally (or in [Dropbox](http://www.dropbox.com)), which are easily opened, searchable, and against which I can run a shell script if needed.
4. WordPress is slow.  Even in the Rackspace Cloud it was slow.  With WordPress, unless you implement a caching strategy using various plugins, every page is dynamically generated.  My content doesn't change very often and older posts never change.  There is no reason to have 100% of my website pages generated on demand.
5. Keeping plugins up-to-date is a pain.  I love the idea of a plugin architecture but when WordPress itself is updated, there's a chance that the update contains changes which break existing plugins.  It's up to the plugin author to react to these changes and provide an updated version of the broken plugin which is compatible with the new version of WordPress.  Once the updated plugin is available, you, as blog admin, still need to notice the update is available then install the updated plugin.

### Nice Features

The main advantage of WordPress is that it separates your content from its presentation.  Octopress retains this feature but has some other advantages:

1.  Octopress takes my raw post content and generates static HTML pages, one for each post and the appropriate index pages.
2. Octopress creates nicely formatted URL slugs for search engine optimization out of the box.
3. I still have complete control over my stylesheets, layouts, etc.
4. All of my posts are stored as simple text files.  In my case, I store them in Dropbox so that I can access them from my laptop, iPad, iPhone, etc.
5. I edit my posts in [Byword](http://bywordapp.com) on both iOS and Mac.  I write in Markdown and get a nice preview as needed.

### Easy Automation

Beyond the features included with Octopress, I've also done a few steps to make publishing new posts easier:

1.  I created an [Alfred](http://www.alfredapp.com) extension which runs a script that creates a new post, titled with the text I provided in the Alfred popup.  The script is basically a streamlined extraction of the new_post rake task provided in the Octopress installation.
2. I have a cron job which runs the rake generate task every 15 minutes and then runs rsync to push the changes up to my Linode server.
3. I have an [IFTTT](http://www.ifttt.com) recipe which monitors my blog and automatically tweets the existence of a new post.

So, basically, I've automated the creation/stubbing of a new post, the publishing of that post, and the Twitter notification of a newly published post.  I'll post more about how this works in the future.

### Optimizations Needed

Octopress uses a particular naming convention for post files which is somewhat cumbersome to work with.  While the creation of new posts is easily automated on the Mac, including proper filename generation, I have yet to find an iOS app which provides a way to easily name a file in Dropbox with this convention.  I very well may write my own utility app to simply start a new Dropbox file with the correct naming.

While having each post as a separate file is an ideal long-term storage solution, it would be great to have an app which loads them all up, indexes them, sorts out the categories and tags, and allows you to drag-and-drop posts for easier retagging, etc.  Alternatively I can still script these sorts of changes.