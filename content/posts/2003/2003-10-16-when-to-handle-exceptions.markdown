---
date: '2003-10-16 10:01:00'
layout: post
slug: when-to-handle-exceptions
draft: false
title: When to Handle Exceptions
wordpress_id: '8'
tags:
- Tips and Tricks
---

I recently worked on a web application where the general philosophy behind exception handling was that every method would catch any exceptions that occurred in the method. The reasoning behind this is that when an exception occurs, its effects would be contained and the executing page would continue to render successfully. When exceptions occurred in this application, certain parts of a page might show up blank while other parts of the page would render normally.

This method of exception handling has an interesting problem. The first issue is that the user has no idea why the application is working in an unexpected manner. For example, in this application, if authentication has failed because the Active Directory server is not available, the login page simply refreshes and reports no error messages.

You should catch exceptions in your code only if you can answer yes to one or more of these questions:



	
  * Will I attempt to recover from the error in the catch block?

	
  * Will I log the exception information in a log file or in the system Event Log?

	
  * Will I add relevant information to the exception and rethrow it?

	
  * Will I execute cleanup code that must run even if an exception occurs?


In the case where you cannot answer yes to any of these questions, you should not handle the exception in the method and let it propagate to the calling code where it might be handled more effectively.

Remember, though, as a general rule in a web application, do not throw exceptions unless absolutely necessary. Throwing exceptions is a very expensive process (in terms of CPU usage) and can significantly hinder the performance of your web application. If you expect that an exception condition might occur in a routine, check for the condition and handle it without using throw.
