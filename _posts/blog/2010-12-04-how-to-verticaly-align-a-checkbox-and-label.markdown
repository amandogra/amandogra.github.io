---
layout: article
title: How to verticaly align a checkbox and label
date: 2010-12-04 21:16:00.000000000 -08:00
type: post
categories: blog
published: true
status: unpublish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra Aman Dogra
  first_name: ''
  last_name: ''
author: Aman Dogra
---
The situation is like this. You have a checkbox and a label with small font size
just next to this as shown in the code below:
```
<input type="checkbox" /><label style="font-size: 10px;">This is the label</label>
```
This will be displayed as:

This is the label

Notice that the text is not vertically aligned with the checkbox. To
make it aligned vertically to the middle of the checkbox we can add
following style to the label\
`position: relative;top: -2px;`\
So the code becomes:\
`<input type="checkbox" /><label style="font-size: 10px;position: relative;top: -2px;">This is the label</label>`\
and it will be displayed as:

This is the label

Now see that the text is vertically aligned to the checkbox.

Adjust the value of top according to the font size and you are good to
go.

<div class="blogger-post-footer">

![](%7B%7B%20site.baseurl%20%7D%7D/assets/){width="1" height="1"}

</div>
