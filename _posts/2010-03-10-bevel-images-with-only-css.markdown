---
layout: post
title: 'Bevel Images with only CSS'
date: 2010-03-10 08:36:00.000000000 -08:00
type: post
published: true
status: publish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra
  blogger_5b414faa76516d87e0b4b243ad1d0e3b_permalink: '7242705486134891153'
author: Aman Dogra
---

CSS method for adding a beveled effect to images like this:

![Storm Troopers](https://amandogra.files.wordpress.com/2010/03/rgbaborders-eg2.jpg)
<!--more-->

    CSS:

    span.bevel {
    position:relative;
    width:200px; /*width of image*/
    height:200px; /*height of image*/
    display:block;
    }
    span.bevel span {
    position:absolute;
    left:0;
    top:0;
    display:block;
    width:190px; /*width of image - 2(width of bevel*/
    height:190px;/*height of image - 2(height of bevel)*/
    border:5px solid;
    border-color:#fff #000 #000 #fff;
    filter:alpha(opacity=40);
    opacity:0.4;
    }



    HTML:

    <span class="beveled">
    <img src="http://www.blogger.com/stormtroopers.jpg" alt="LegoStormtroopers" />
    <span></span></span>
    <!--Do NOT remove this extra span-->
