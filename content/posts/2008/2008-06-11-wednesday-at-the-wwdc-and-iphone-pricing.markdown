---
date: '2008-06-11 14:53:46'
layout: post
status: publish
title: Wednesday at the WWDC and iPhone Application Pricing
tags:
- WWDC
---

My posting velocity on both CharlesSieg.com and via Twitter is decreasing a bit.  There are a couple of reasons for that.  One is that most of the stuff we hear during the daily sessions is covered by NDA and, while some people feel free to disregard that, I'm all about not biting the hand that feeds me.  So no sneaky posts from me. Private conversations with me, however, is another story.  Second, there is quite simply a lot of work to be done and work takes priority over blogging.  I'm at the conference all day and then I put in at least another 8 hours in front of the computer at night working on my code and trying out some of the techniques picked up during the day.  Last night, for instance, I went to bed at around 5am Pacific time...  Today I am taking a lighter day, getting back in sync with Illinois time and, hence, the break for a little blogging.

Yesterday's sessions were mostly on the graphics architecture of the Mac and the iPhone.  I firmly believe that what sets one application above another - all other things being equal - is the presentation and look of an application.  It's this graphics work that takes the bulk of time, actually, when writing an iPhone application.  Spend some time looking at how the Weather app works on the iPhone and you'll see what I mean.  When you slide the current view but then let it go before it switches to the next, the view slides cleanly back into place with a little "bump" at the end.  It's little things like this that the customer picks up subconsciously as "cool" and which take developers like me a ton of time in coding.

Now that's not to say that animating views with Cocoa Touch on the iPhone is hard - it's not - but tweaking them takes time.  Some animations are actually multiple animations chained together, choreographed like a ballet.  That's what you see with native Apple applications and that's what I strive for with my iPhone applications.  That's also why all of the sessions I am attending this week are around mastering the graphics architecture and animation.

Let me give you an example.  The [AccelaStudy](http://www.accelastudy.com) application that I have built is all about learning vocabulary.  At this point, it looks like we will be releasing 6 applications on July 11th.  The first one is an application that will teach you over 500 new English vocabulary words, most of which have been used on the GRE, GMAT, SAT, ACT, and CLEP examinations.  These are words like apocryphal and voluble.  Words not often used in day to day conversation but which are used constantly in books, magazines, and other press.  If you don't believe me, look [here for apocryphal](http://news.google.com/news?hl=en&ned=us&q=apocryphal&btnG=Search+News) and [here for voluble](http://news.google.com/news?hl=en&ned=us&q=voluble&btnG=Search).  A lot of people buy various products to help them study these words.  There are decks of flashcards and little reference books and study guides.  All of them serve the same purpose and they all have the same issues: heavy, bulky, non-interactive.  It's not like you can be standing in line at Chipotle, blowing off 20 minutes of your day, and whip out a deck of flashcards and start studying.

But with AccelaStudy on the iPhone, you can.  You can literally study anytime, any place.  Over 500 words in the palm of your hand.  And AccelaStudy is interactive - it helps you test yourself on what you have learned by building dynamic quizzes.

But back to my example...  When I decided that a vocabulary application like AccelaStudy would be a good idea, I surveyed the "competition" and this is what I found:

![iStudy](http://img221.imageshack.us/img221/7286/img90151vq4.png)

That's a freeware app called "iStudy" which, at the time, required a jailbroken phone.  It looks like a nice iPhone application.  But it isn't compelling, it's not elegant or beautiful.  This is AccelaStudy:

[![](http://www.charlessieg.com/wp-content/uploads/2008/06/screenshot.png)](http://www.charlessieg.com/wp-content/uploads/2008/06/screenshot.png)

Which one is the one you want to spend your time with?  AccelaStudy has great content but the bulk of development time was spent making it look great and making it very smooth and intuitive to use.  It has smooth transitions, rotations from front-to-back, and very intuitive finger gestures.

We are also releasing 5 foreign language products for building French, Spanish, German, Italian, and Turkish vocabulary.  Each of these products will have over 1,000 commonly used vocabulary words.  There are other products planned for later this year.

So, this brings up an interesting question.  How much should we charge for AccelaStudy products?  There is a lot of discussion about this at the WWDC.  Various media people are running around trying to get an idea of this also.  A Piper Jaffray analyst is saying that it looks like [the average price of an iPhone application](http://www.appleinsider.com/articles/08/06/11/wwdc_survey_suggests_70_of_planned_iphone_apps_may_be_free.html) will be $3.00 or less.  The guy interviewed 20 people at random.  20 people out of 5,200.  And he certainly didn't interview me.

So what he is saying is, that the average price of an iPhone application will be less than the cost of a gallon of gasoline in the United States.  I don't think so.  A guy like me puts in over 400 hours minimum to get an application to a production-ready state.  This means developed, debugged (no memory leaks!), performance tested, deployed on hardware and tested again.  This means vocabulary data authored, proofed, proofed again, transferred into optimized binary formats.  This means graphics design, website support, marketing materials and website, and the whole interaction with Apple and provisioning profiles, etc.  Applications like iStudy above may be $3.00 or less.  They may even be free.  But any professional software development company is going to want a return on the significant investment put into developing an iPhone application.

But in the end, the cost will still be relatively low.  The application is going to be out in front of a massive number of potential customers.  The App Store is going out to 62 countries this year, with more to come.  There are 6 million iPhone users now, with Apple aiming for 10 million in 2008, and some industry observers predicting 25 million.  By the end of 2009 we will be looking at 50 million iPhones.  So it is possible to spread that return on investment across a very large customer base.

So back to the question of price.  You can go to Amazon.com and pick up a deck of GRE/GMAT flashcards for around $10.  There are [similar vocabulary products](http://www.amazon.com/Kaplan-GRE-Exam-Box/dp/1419552201/ref=pd_bbs_sr_1?ie=UTF8&s=books&qid=1213221052&sr=8-1) that go up to $20.  These, of course, still have all of the issues of bulk, etc.  We will be charging $14.99 a copy for AccelaStudy.  After Apple's cut, we get $10.50 per copy.  I think that's pretty reasonable.  A vocabulary study product for less than what will shortly be the cost of 3 gallons of gasoline.  Puts a little perspective on things, does it not?
