---
date: '2004-01-15 06:45:00'
layout: post
slug: get-architects-involved-early
draft: false
title: Get Architects Involved Early
wordpress_id: '255'
---

**Problem**  

I recently became aware of a project to upgrade an existing system. This particular system was not a paragon of best practices. The new requirements that were handed to the development team specify changes to the architecture which would again violate best practices, making the system worse than before. How can requirements be gathered which do not adversely impact architecture? How can architects avoid this scenario?  

  

**Story 1**  

When I was about 6 years old, my parents took me to a steakhouse for my birthday. I was just learning to read and my only request to my parents on that occasion was that I be allowed to order â€œwhat I wantâ€ from the menu without any help from them. They agreed and we all went happily to the restaurant and I was looking forward to demonstrating my independence.  

  

All I wanted that evening was â€œsteakâ€ and I knew how to read well enough to recognize the word â€œsteakâ€. However, when the menu was presented, I found that there were lots of items on the menu which said â€œsteakâ€. I was confused â€“ I only expected one â€œsteakâ€ to be there. So when it came time to order I realized I had to pick one of these â€œsteaksâ€ for my dinner. Well, I happened to like fish a lot also and was able to recognize the word â€œtartareâ€ on the menu, although I was certain that they had spelled it wrong. I couldnâ€™t read anything else about it but I figured it was a steak with tartar sauce on top and if I ordered that I could just scrape off the sauce and go on, merrily, with my dinner.  

  

When I placed my order, my parents immediately tried to suggest something else. I am pretty sure I remember my mother saying something like â€œOh, honey, you wonâ€™t like that, why donâ€™t you try this?â€ I was furious!!! How dare they attempt to assist me in my decision?!?! The only thing I wanted was to make my own decision without any help from them. I was absolutely SURE that steak tartare was exactly what I wanted. So they let me order it.  

  

Most people know what steak tartare is but if you donâ€™t, itâ€™s essentially a ball of [raw hamburger](http://www.thestranger.com/2002-02-07/chow-1.jpg). I suppose itâ€™s tasty if youâ€™re into that raw sort of thing. But when my steak tartare appeared on the table, I knew there had been a mistake. There was no way that pink ballish-thing could be the steak I had asked for. My parents explained to me that this was, indeed, steak tartare. Needless to say I was very upset. My parents did not allow me to get something else. I learned a good lesson. In addition, after that I was probably the only 7 year old in Carlock who knew how to spell both â€œtartarâ€ and â€œtartareâ€.  

  

However, customers do not like to be on the receiving end of this kind of lesson. And yet how many times have we seen customers who specify "exactly" what they want only to reject what the get when the system is built? What can be done to prevent this from happening?  

  

**Story 2**  

In southern California there is a church called the [Crystal Cathedral](http://www.crystalcathedral.org/visitors/images/welcome.jpg). It is a breathtaking building, made almost entirely of glass. It is certainly one of the most beautiful religious structures in the world. The minister of that church, Robert Schuller, had envisioned a church of glass many years before he met with the architect to begin the project.  

  

When the architect came back with his first set of drawings for the church, it was a building with four walls of concrete and a glass ceiling. Schuller said that he wanted the entire building to be glass, including the walls. The architect went back to the drawing board and came back with the design of the church that exists [today](http://www.seeing-stars.com/ImagePages/CrystalCathedralPhoto2.shtml).  

  

However, when Schuller saw the second drawings, he was still not satisfied. He wanted each wall to be a sheer, single piece of glass. What the architect had drawn was a wall of [glass latticework](http://www.seeing-stars.com/ImagePages/CrystalCathedralPhoto4.shtml) similar to a honeycomb. Schuller was patient, though, and listened to the architectâ€™s reasoning. In SoCal, it was impossible to put up glass walls the way Schuller originally envisioned. No glass could withstand the passing earthquakes prevalent in the region. Also, if one of the walls were to shatter, the amount of broken glass could easily injure or kill someone, and would be very expensive to replace. What Schuller realized was that what we wanted, really, was a church bathed in sunlight, full of light passing through glass. He was not set on walls completely made of glass â€“ the light was the important part. In the end, the latticework design was approved. Schuller got a church of light and the architect built a beautiful, but very safe, structure.  

  

The outcome of Schuller's church was a lot better than the ending of my birthday meal. Why was it a different conclusion? Why was Schuller happy with his product and I was so unhappy with mine?  

  

**Analysis**  

In both stories, the customers wanted something specific but were unable to clearly describe it upfront. I had originally wanted â€œsteakâ€ but what I really wanted was a cut of beef, medium well, in a single piece, hot and juicy. What Schuller originally wanted was a church with glass walls and ceiling but what he really wanted was a church filled with sunlight.  

  

In constructing systems for business users, the customer cannot be allowed to dictate the architecture of system. Certainly the customer can specify requirements in usability, performance, availability, and in other measurements of the quality of a system. But the implementation of these requirements into a working system is the responsibility of the architect. If the customer is demanding something in the architecture which is improper, the architect needs to coach that customer and educate them as to why it is improper.  

  

Too many times developers will go along with a customerâ€™s architectural demands knowing that they are building a piece of garbage but building it anyway â€œbecause the customer wants it that wayâ€. Thatâ€™s totally wrong. The customer doesnâ€™t want it that way, they just donâ€™t have a better idea or they havenâ€™t thought it through well enough. What they want can usually be abstracted into something less concrete such as â€œprevasive sunlightâ€.  

  

There may be cases where the customer is technically savvy enough to put some specifications on the architecture, such as location of servers or choice of back-end software. There may be existing systems which must be used which are not built on best practices. In these scenarios it is extremely important to keep from making these systems worse. Any additions or modifications to the system must be made according to best practices. Whatever is built must lead the way toward better architecture rather than extend the disarray that is currently present.  

  

The lesson here is that architects need to get involved early on in the lifecycle of a project. They need to be listening in when requirements are gathered to ensure that the requirements do not place unrealistic demands on architecture. Architects need to be assertive but diplomatic in coaching customers into making the right choices. Without architectural guidance throughout the process, projects will probably fail, and if they don't fail they will be much less successful than they could have been.  

  

Want to share your thoughts on this topic? Add your comments below.  

  

_* Note: This is a first draft. *_  


