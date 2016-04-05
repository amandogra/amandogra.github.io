---
layout: article
title: Use non web-safe fonts on webpages
date: 2011-06-08 19:52:38.000000000 -07:00
type: post
categories: blog
published: true
status: publish
categories: []
tags: []
meta:
  _edit_last: '13563105'
  _oembed_91935cca26f100802f3a57cffdf9a7ca: '{{unknown}}'
  _oembed_979e827c6fdce6a714cc7d29bdf58ec4: '{{unknown}}'
  _oembed_bcaff65f29e27b60b4dbba3fcd4a4024: '{{unknown}}'
  _oembed_29d079aa88e0fd9d4e2be85d8e0deac2: '{{unknown}}'
author: Aman Dogra
---

Have you ever thought of using a special font on your webpage and then
ended up using some boring web-safe font or an image instead just
because the font was not web-safe? Well, now the designers don't have to
compromise as now we have techniques which can be used to load the
specific font you want on your webpage.
<!--more-->
A beautiful font is also as much a part of beautiful design as the good
images are. Before the entry of HTML5, web-designers were using only
web-safe fonts. What are web-safe fonts? Why only web-safe fonts are
used for web platform? The websites are viewed on different platforms.
Different fonts are installed on different platforms. All types of fonts
are not installed on a single machine. For example, a Mac machine does
NOT has 'Trebuchet MS' whereas the Windows machine does not has 'Apple
Garamond' font on it. So, the web-safe fonts are those fonts which are
available on all or most of the platforms, like 'Arial' or 'Verdana'.
Creating websites using web-safe fonts is a good practice as the text on
your website will be displayed similar on all the platforms.

But at times using web-safe font is not stylish. There might be times
when you have craved to use that special font in your header and end up
using some boring font or an image instead. Well, now we don't have to
compromise as now we have techniques which can be used to load the
specific font you want on your webpage. There are many techniques like
[cufon](http://cufon.shoqolate.com/generate/ "cufon"),
[siFR](http://www.sifrgenerator.com/ "siFR") ,
[type-kit](http://typekit.com) to solve this issue. But all these
methods have different issues, like in 'cufon' you can not select the
text, 'siFR' uses Flash to embed the font into the webpages and
'type-kit' is not completely free. The method which I am going to
discuss today is a bit different from these techniques as it is simple
CSS. It's known as **@font-face** method.

**Choose the font**

Enough talk, now let's see how to use @font-face method. First of all
choose the font you want to use. Some good resources to choose a font
are as below:

<http://www.dafont.com/>

<http://fontdeck.com/>

<http://www.fontsquirrel.com/>

**Generate a web-font-kit**

Once you have downloaded the font, open
<http://www.fontsquirrel.com/fontface/generator> and add the font to the
@font-face Kit Generator

[![](%7B%7B%20site.baseurl%20%7D%7D/assets/font-gen1.png){.alignnone
.size-full .wp-image-156 width="617"
height="351"}](http://www.survah.com/wp-content/uploads/2011/06/font-gen1.png)

Once you choose a font from the 'Add font' dialog box, it will start
generating he web-font-kit.

[![](%7B%7B%20site.baseurl%20%7D%7D/assets/font-gen2.png){.alignnone
.size-full .wp-image-157 width="616"
height="359"}](http://www.survah.com/wp-content/uploads/2011/06/font-gen2.png)

Once the @web-font-kit is ready for download, the Choose 'Optimal' if
you do not know much about font optimization. Check the checkbox and
click on 'Download You Kit'

**Keep the fonts at appropriate location**

Extract the contents of the webfontkit-xxxx.zip file which is downloaded
as kit. You'll observe that there are several files starting with the
name of the font. These files contain the font in different formats like
.eot, .svg, .ttf, .woff . All these the necessary as different platforms
understand different formats of font.

Copy these four files to a location in your server. For the purpose of
this tutorial I have placed these files in the same location where the
css file is.

**Adding the @font-face rule in CSS**

Now that our fonts are at right location, lets add the rule which is
going to do the magic. In your CSS file, add a code (as above as
possible) as follows:

{code type=css}\
@font-face {\
font-family: 'nameOfYourFont';\
src: url('nameofyourfont-webfont.eot');\
src: url('nameofyourfont-webfont.eot?\#iefix')
format('embedded-opentype'),\
url('nameofyourfont-webfont.woff') format('woff'),\
url('nameofyourfont-webfont.ttf') format('truetype'),\
url('nameofyourfont-webfont.svg\#BebasNeueRegular') format('svg');\
font-weight: normal;\
font-style: normal;\
{/code}

In this code the url() will point to the paths of the fonts copied in
the last step and 'nameOfYourFont' will be replaced by the name of the
font you generated (It could be anything except the names of default web
fonts). An easy way of doing it is to copy the content of the style.css
file which is found in the folder which was extracted in the last step.\
Syntax is sefl-explanatory. We are creating a new font-family by loading
the font from a specific location on server. We can now simply use this
font-family in our CSS anywhere. For example,\
{code type=css}\
p { font-family: nameOfYourFont, Arial, san-serif; font-size: 12px}\
{/code}\
Now all the &lt;p&gt; elements on the webpage will be displayed in the
new font. You can use as many @font-face definitions as you require.
This blog is also using a @font-face for the main navigation. You may
check that in the CSS file.

**Conclusion**

Creating a web font-family is not difficult now. Just convert the
selected font into different formats. Place them on your server. Define
a @font-face and use the font like any other font family. I hope you
enjoyed the tutorial and now you'll be using beautiful fonts in any
webpage you like.\
Happy coding!
