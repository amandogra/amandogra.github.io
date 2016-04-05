---
layout: article
title: 'Using cyclic function in javascript'
date: 2010-03-10 16:47:00.000000000 -08:00
type: post
categories: blog
published: true
status: publish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra
  blogger_5b414faa76516d87e0b4b243ad1d0e3b_permalink: '7661759105064235940'
author: Aman Dogra
---

Recently I was working on a design for our client '[Your Tribute](http://www.yourtribute.in)'. For this design, a slide show was
required. One can find a number of slideshows on Internet, but the
glitch with this one was it was having bullets related to each image and
this slideshow could be paused by hovering over any of these bullets.
<!--more-->
You can have details by having a look at Your Tribute's
[website](http://www.yourtribute.in/).

The difficulty here is that if user hovers over a bullet (or side tabs)
then the respective slide should be displayed and once the user
hovers-out of the bullet then the slide-show should resume.\
After searching for long on Internet, I decided to write one jQuery
plugin for this slideshow by myself.

While working on this I learnt the difference between setTimeout and
setInterval. I also used the clearInterval to interrupt the time
interval ion javascript.

Whenever we have to use recursive functions like this:

`function recrFunc(){.. setTimeout('recrFunc();', 10000);..}`

...then it's better to use setInterval() function something like this:

`timeoutid = setInterval('recrFunc();', 10000);function recrFunc(){...}`

... the use of setInterval function is that this time can be cleared
anytime by using clearInterval() function like this:

`clearInterval(timeoutid);`

So, crux of the story is that if you have to call a function recursively
after a specific time interval then use setInterval instead of
setTimeout and if you have to call a function only once after pausing
for a specific time period then use setTimeout

<div class="blogger-post-footer">

![](%7B%7B%20site.baseurl%20%7D%7D/assets/7129060648210934577-7661759105064235940?l=meraaaj.blogspot.com){width="1"
height="1"}

</div>
