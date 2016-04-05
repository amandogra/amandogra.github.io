---
layout: article
title: Add a placeholder to the input box
date: 2012-08-25 09:23:50.000000000 -07:00
type: post
categories: blog
published: true
status: unpublish
categories: []
tags: []
author: Aman Dogra
---

Among the many awesome features of CSS3, there is a feature known as
'placeholder'. Placeholder is a text which is displayed inside the input
text box on HTML page. You must have seen something like.

\[caption id="attachment\_115" align="alignnone"
width="138"\][![placeholder](%7B%7B%20site.baseurl%20%7D%7D/assets/screen-shot-2012-08-25-at-2-32-40-pm.png "Placeholder"){.size-full
.wp-image-115 width="138"
height="41"}](http://amandogra.files.wordpress.com/2012/08/screen-shot-2012-08-25-at-2-32-40-pm.png)
A placeholder text inside the input box\[/caption\]

This can be achieved very easily by adding &lt;input type="text"
 placeholder="Name"/&gt;. But the issue is that each browser handled it
differently. There are browsers like IE (ahem) which do not support it
and there are browsers like Firefox, Chrome, Opera and Safari, which
support 'placeholder' but has different behavior towards it.

For example, in Firefox, default color of the placeholder is black while
in it is silver in Chrome or Safari. Moreover when we click/focus on the
input box, it disappears immediately. I like the placeholder handling
done by Safari.

In Safari, when the user clicks on the input box the placeholder text
does not goes away. It only disappears when user enters some value
inside the text-box

So, here is the jsFiddle for the placeholder. It's a simple jQuery
plugin which you can understand just by looking at it.

http://jsfiddle.net/amandogra/eDb2T/

If something is unclear or if there are any bugs in there, feel free to
[contact me](mailto:amandogra@gmail.com)
