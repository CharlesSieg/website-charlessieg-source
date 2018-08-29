---
date: '2008-06-06 11:33:56'
layout: post
draft: false
title: Versions and Beanstalk
tags:
- Apple
- Source Control
---

I recently decided to start using source control for my Mac software development.  Yes, yes, I use source control - [Subversion](http://subversion.tigris.org/) - all day long at work but had not gotten around to using it at home for other projects.  One of the reasons is that I simply don't want the hassle of setting everything up.  I want to code, not fool around with the administrative tedium of doing backups, maintaining a repository, setting up SSL and securing the server, etc.  I have one dedicated server and that is enough trouble as is.

So I decided to outsource my source control hosting.  There are some obvious concerns about the security and privacy of having my source in someone else's servers.  But I have an optimistic view and do not really believe that the upstanding employees of the source control hosting company are out to steal my software.  Perhaps if I was writing something really, really unique and special, that might be different.  But, really, I just want a repository to put my code in where someone else will watch over the other stuff.

[Versions](http://www.versionsapp.com/) is a new (beta) Subversion client for Mac OS X.  It is made by the same company that makes [Beanstalk](http://www.beanstalkapp.com), a hosted source control provider.  Usually when you can get two complementary products from the same company, it is best to do so since they often have synergies that other products would not have.

This is certainly the case with Versions and Beanstalk.  After installing Versions and running it, it presents you with a nice way to pop out to Beanstalk, set up an account, set up a repository, and get started right away.  This is what I did and I had my repository running within minutes, making my first commit immediately thereafter.

Versions works a lot like [Tortoise](http://tortoisesvn.tigris.org/) in the Windows world but it has one great little feature I really wish Tortoise had.  Versions recognizes when you delete a file and it recognizes when new files are added.  It does not actually do the Subversion Delete and Add commands but it displays icons for those files which draw your attention to them so you can manually do the Delete and Add.  Many a build has been broken because a developer forgot to formally Add his new class file to the repository.  Versions makes it harder for the developer to make this common mistake.

Beanstalk has excellent integration with other 3rd party web applications, including [Basecamp](http://www.basecamphq.com/), [Harvest](http://www.getharvest.com/), [Twitter](http://twitter.com), and [Lighthouse](http://www.lighthouseapp.com/).  I'm using Lighthouse with Beanstalk to automatically track which commits are tied to cases.  Each repository in Beanstalk also exposes its commit log as an Atom/RSS feed so I can get a running log of commit activity in [my news reader](http://www.newsgator.com/Individuals/NetNewsWire/default.aspx).

All in all, both products are compelling and highly recommended.
