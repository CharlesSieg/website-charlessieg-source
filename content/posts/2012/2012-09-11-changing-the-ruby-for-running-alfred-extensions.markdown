---
layout: post
title: "Changing the Ruby for Running Alfred Extensions"
date: 2012-09-11 15:17
comments: false
tags: 
- Ruby
- Alfred
- Blogging
published: true
---

I recently wrote [a post](http://www.charlessieg.com/blog/2012/09/07/New-Blogging-Software/) about how I moved over to Octopress for blogging and I discussed the small difficulty in naming a new post file.  It's an inconvenience, really, but as they say: death by 1,000 cuts!

To alleviate this, I created a simple Ruby script, based primarily off of the [Octopress](http://www.octopress.org)-included rake task, that creates a new post.  More on that script later but I ran into a problem running my script with [Alfred](http://alfredapp.com).

<!--more-->

I found that running the script with the Silent option enabled was not working - the script was not running.  Turn off the Silent option and the script ran fine.

### What's the problem?

The problem is that scripts running from Alfred run using the system installation of Ruby.  This is the one in /usr/bin and not the one that you probably have installed in your home directory.  If your script relies on the Ruby version in your home directory the script will fail.  If your script requires a Ruby gem that is only installed in your home directory, the script will fail.

### How to fix this?

First, the solution is **NOT** to update your system Ruby or install your Ruby gems in a system directory.  Speaking from a Mac OS X perspective, Apple OS installs and updates manage the system Ruby and some Apple software depends on that Ruby staying, essentially, pristine.  If you muck it up, that software may no longer run correctly in the future.  The solution is to somehow indicate the Ruby that your script needs to run and make sure the script is run using that Ruby.

I found [this post](https://getsatisfaction.com/alfredapp/topics/make_an_option_to_load_users_bash_profile_when_executing_bash_scripts_in_silent_mode) after much searching in Alfred's own [GetSatisfaction site](https://getsatisfaction.com/alfredapp).  The solution is to add this line of code to the top of your script or in the Command textarea when creating a new script extension in Alfred:

{% codeblock This line makes the script use your local Ruby instead of the system Ruby. - script.sh %}
[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm"
{% endcodeblock %}

This line of code has to be added to each script extension that you want to run with your home installation of Ruby.  There is a similar solution to this problem for scheduling Ruby scripts to be run by cron that I will cover in another post.