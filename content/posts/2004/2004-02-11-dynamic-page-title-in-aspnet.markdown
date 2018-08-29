---
date: '2004-02-11 14:37:00'
layout: post
slug: dynamic-page-title-in-aspnet
draft: false
title: Dynamic Page Title in ASP.NET
wordpress_id: '5'
tags:
- ASP.NET
- Tips and Tricks
---

Ever since I started writing .NET code, I've been irritated that there seemed to be no way to programmatically set the TITLE tag of a web page from the code-behind. Certainly you can do things like

`<title><% = msTitle %></title>`

but I never found a way to set it in the code-behind. Always seemed to me that there should be something like

`Page.Title = "My Title";`

Today, thanks to someone's posting on [GeeksWithBlogs.net](http://www.geekswithblogs.net/), I now know how this works. Essentially you set the TITLE tag like this:

`<title id="pagetitle" runat="server" />`

Then you can place this code in the code-behind:

`
**protected** System.Web.UI.HtmlControls.HtmlGenericControl pagetitle;`

` `

`**private** void Page_Load( object sender, EventArgs e )
{
pagetitle.Value = "My Title";
}
`
