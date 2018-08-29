---
date: '2008-06-06 11:59:51'
layout: post
draft: false
title: Untrusted SLL Certificate Problems with Versions and Beanstalk
tags:
- Source Control
---

I did end up having a bit of trouble with [Versions](http://www.versionsapp.com/) and [Beanstalk](http://www.beanstalkapp.com).  It happened when I upgraded my Beanstalk account to a paid account and, as part of the upgrade, got HTTPS connectivity to my repositories.

When I changed the repository URL in Versions from the original HTTP version to the new HTTPS one, I ran into an error:

    
    Server certificate verification failed: issuer is not trusted


There was more to it than that but that was the important part.  Not being deeply familiar with Subversion (or Beanstalk or Versions), I pinged their tech support...at about 3 in the morning.  We went through a round of emails but I was eventually left with:


> Talking about https problem, there is a bug in Versions that prevents usage of Beanstalk accounts over SSL. You can fix that by accepting the certificate in your command line.


I pinged back asking what that command line command might be but no response, and no response since (12 hours later).  So maybe I burned the guy out and he needed an extended nappy nap.

But I researched into it and found that the issue is common with the checkout command when hitting a Subversion repository over HTTPS.  The trick is that you need to do this once with the command line - where Subversion will prompt you to accept the certificate (which I did, permanently) - and then your future use of this repository, even through clients such as Versions, will work without issue.

So simply open a Terminal window and type:

    
    svn co "https://<XXXXXXXX.svn.beanstalkapp.com>/<your_repository_name>/"


When the prompt comes up to accept the certificate, make your choice.

So, contrary to what the support guy said, it isn't really a bug with Versions.  It's a normal security issue with Subversion and maybe Versions could be a little better and handle this automatically.  But maybe, until it does, tech support might want to keep that little command handy for source control n00bs like me...who are still happy to pay good money every month for them to host my source.

But I'm still loving both Version and Beanstalk.

UPDATE:  Not sure when this showed up, but they now have a help topic on this issue: https://help.beanstalkapp.com/articles/16-getting-around-certificate-validation-error

It may always have been, there, not sure.  Perhaps the tech support guy can point the next guy to have this issue here.
