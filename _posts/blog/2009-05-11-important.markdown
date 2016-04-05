---
layout: article
title: '!important'
date: 2009-05-11 10:51:00.000000000 -07:00
type: post
categories: blog
published: true
status: publish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra
  blogger_5b414faa76516d87e0b4b243ad1d0e3b_permalink: '4363568448942359356'
author: Aman Dogra
---

I know I am a bit late in understanding this concept, but it's
better if it's later than never. I learnt about the property today. This
keyword is used in CSS to tell the browser that whichever rule has the
!important property will always be applied no matter where that rule
appears in the CSS document. So if you wanted to make sure that a
property always applied, you would add the !important property to the
tag.
<!--more-->

The best use of this property is the famous 'Holy Hack for IE'. I am
sure if you have ever worked on rounded corners with images, then you
have encountered that everything works fine in all other browsers but in
IE, there is an issue of 2 pixels. I'll explain that some other day. For
now the fix is !important property.

For example,

```css
.inner-form {
    width:648px !important;
    width: 650px;
    background-color:#FFFFE5;
    border-left: solid 1px #D4D4D5;
    border-right: solid 1px #D4D4D5;
}
```

In this code, notice that the width
is being defined two times. This is to trick the IE6 browser. What this
code is doing that it is telling all the browsers that width 648px is an
important thing. Mind it! BUT as we all know that IE is one of the
dumbest browser, which is unable to interpret the !important tag. Which
in a way is good for us. We can now trick the IE by telling that width
should be 650px ;) This solves our 2px problem.
