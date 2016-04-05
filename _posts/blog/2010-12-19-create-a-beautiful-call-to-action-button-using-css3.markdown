---
layout: article
title: Create a beautiful call-to-action button using CSS3
date: 2010-12-19 19:08:25.000000000 -08:00
type: post
categories: blog
published: false
status: publish
categories: []
tags: []
meta:
author: Aman Dogra
---

I am in love with CSS3. This has happened a while ago. Since then I've
been following her in every nook and corner of any website or book where
I could find her. She's so beautiful, so adorable, so...<!--more-->

Ok! Ok! before I loose track of what I'm here for, I should stop
praising her and start sharing on how to create a beautiful
call-to-action button using CSS3. Here it goes.

Suppose we have a simple anchor tag like this

```
<a href="#" class="call-to-action" > Click Me! </a>
```

then it will be displayed like:

[Click Me!](#)

Let's add following styles to our 'call-to-action' button:

```
a.call-to-action{
    background-color: #5B9E00;
    border: 3px solid #f2f2f2;
    color: #FFFFFF;
    display: block;
    padding: 8px 10px;
    text-align: center;
    margin: 10px;
    width: 100px;
    text-decoration: none;
    font-weight:bold;
}
a.call-to-action:hover{
    text-decoration: none;
    font-weight:bold;
    background-color: #A6de00;
    border: 3px solid #444;
}
```

Now lets add our dear CSS3 to it by making the corners of this button
round. For this we are just going to add following lines of code to
`a.call-to-action` in our CSS.

```
-webkit-border-radius: 8px;
-moz-border-radius: 8px;
 border-radius: 8px;
```

To make it more handsome with the help of another feature from CSS3.
Lets throw some light over this button and force it to drop some shadow.
Add following line to the a.call-to-action style:

```
text-shadow: 0 1px 1px rgba(0, 0, 0, 0.5);
```

This will drop a shadow of 1px to the right and bottom of the button.
rgba stands for Red Green Black and Alpha. So the color of the shadow
will be black and it will be 50% opaque (or transparent).\
Lets add the shadow to the button itself which will make it stand out,
by adding the following to the CSS:

```
box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
```

This all will be displayed as:

[Click to see the
output](http://jsfiddle.net/amandogra/9NDMz/1/embedded/result/){.call-to-action-one}

See, now we have a beautiful button here. Lets add an effect to the
state when the button is hovered. Add the following lines again to the
style of a.call-to-action button

```
-webkit-transition: background 0.3s ease;
-moz-transition: background 0.3s ease;
-o-transition: background 0.3s ease;
transition: background 0.3s ease;
```

To see what changes it has done, open the same page in Safari or Google
Chrome browsers (browsers which supposrt webkit). You'll see that
instead of instantly changing color when hovered, this button is
gradually changing the color. See for yourself.

[Click to see the
output](http://jsfiddle.net/amandogra/9NDMz/3/embedded/result/){.call-to-action}

With the help of these simple CSS3 features we have created a beautiful
Call to Action button. I know you are going to ask that is this
supported in IE7 or 8. My answer would be is it necessary that a website
should appear the same on all the browsers? I am of the opinion that the
users with better browsers should have better user experience. So, don't
be such an old school, upgrade!

I don't know whether you'll use these techniques but after reading this
I'm sure that you'll fall in love with CSS3, like me.
