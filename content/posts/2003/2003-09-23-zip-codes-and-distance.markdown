---
date: '2003-09-23 14:29:00'
layout: post
slug: zip-codes-and-distance
status: publish
title: Zip Codes and Distance
wordpress_id: '306'
---

Recently I was informed that the [TCF Bank website](http://www.tcfexpress.com/) is not able to provide a list of banks near a given zip code. Surely we have all used a search like this by now. You go to a website, type in your zip code, and the website returns a list of locations which are near the given zip code. You might get a list like this:  

  

TCF Bank Location A, 2.2 miles  

TCF Bank Location B, 4.7 miles  

  

This is pretty common these days but TCF Bank apparently has not gone that extra step to provide the distance. In fact, it just searches the given zip code. So if I type in 60089 and there are no banks with that zip code, the search returns no results. This is the case even if a bank does exist one block past the edge of the 60089 zip code.  

  

Actually, creating a search that does this type of calculation is fairly challenging. How does it work to begin with? It works because there is a database available that has mappings between zip code and latitude and longitude. You can license the database from [here](http://www.zip-codes-latitude-longitude.com/). The company updates the database regularly so when new zip codes are created, the data is entered into the database.  

  

My first experience with this was on the [GM BuyPower](http://www.gmbuypower.com/splash.html) project. We used the zip code database to find the closest GM dealership for a potential customer. This worked fine for dealerships in the United States but we ran into all kinds of trouble when we tried to bring the system up in Australia. As it turns out, Australian zip codes do not actually correspond easily to latitude and longitude. The postal areas represented might not be related to geography at all and may be oriented to "all military posts in south Australia" for example. A postal area might curve around other postal areas depending on street layout. Needless to say the business analysts had a tough time getting the requirements right on that one.  

  

My wife tells me that until she was in her mid-teens, Istanbul, Turkey didn't even use zip codes. There was just an address and a city name. It was up to the individual postmen to find a particular address. I have no idea how the sorting of the mail was worked out. My mother-in-law has had the same postman for 20 years. In Turkey, postmen are sometimes tipped when they deliver important mail. If you tip them right, they will also do some "junk mail" filtering for you, too. The junk mail will be left in the mailbox while the important mail is then hand delivered. Too bad you can't tip your email program to filter out all the spam...

