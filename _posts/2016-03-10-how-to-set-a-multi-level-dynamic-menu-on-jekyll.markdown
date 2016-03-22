---
layout: post
title: "How to Set a Multi-level Dynamic Menu on Jekyll"
date: 2016-03-10T12:37:28-08:00
---

I have few pages on my jekyll website such as 'About', 'Blog' pages. Jekyll has a pretty good way of adding the page-links to the top navigation bar.
The only problem which I was facing that I have enabled 'pagination' [Click this to learn how to set pagination on jekyll](#) and as soon as I enabled
it, I started seeing multiple links pointing to 'Blog' in my navigation menu. <!--more--> The reason for that was that all the pages (of pagination) were being considered
as separate `site.pages`. This is not what I wanted, a page for each paginated page as `blog/page1`, `blog/page2` etc. So I ran through the jungle of Web and found that
there are many ways to set it. Few of the ways which I liked are as mentioned below:

## Method 1: Setup a separate configuration file to maintain the menus
As mentioned [here](https://github.com/Painted-Fox/jekyll-site-menus), one could use this plugin and create a separate file to maintain the menu. This way user will have a
lot of control over what goes into the menu and in which order. The only issue with this method is that each time you add a new page, you have to add it to the top-menu. I don't want that, at least not yet.

## Method 2: Use a `liquid` script
As mentioned [here](https://gist.github.com/kasperisager/9416313), one could add a simple script in the navigation.html and make the process of creating menus and submenus automated.
For amandogra.github.io, I have modified this script a bit as I want only first level of pages to be displayed in my website. i.e., pages like `/blog/` or `/about/` and not something like `/blog/page1`.
So the piece of code which I added to display my navigation menu is as follows:

<pre>
<code>
&#123;&#37; assign entries = site.pages | sort: "path" &#37;&#125;
&#123;&#37; for entry in entries &#37;&#125;

&#123;&#37; capture slug    &#37;&#125;&#123;&#123; entry.url | split: "/"   | last                       &#125;&#125;&#123;&#37; endcapture &#37;&#125;
&#123;&#37; capture current &#37;&#125;&#123;&#123; entry.url | remove: slug | remove: "//" | append: "/" &#125;&#125;&#123;&#37; endcapture &#37;&#125;

&#123;&#37; if '/' == current &#37;&#125;
&#60;a class="page-link &#123;&#37; if page.url == entry.url &#37;&#125;active&#123;&#37; endif &#37;&#125;"
href="&#123;&#123; site.baseurl &#125;&#125;&#123;&#123; entry.url &#125;&#125;"&#62;;&#123;&#123; entry.title &#125;&#125;&#60;;/a&#62;;
&#123;&#37; endif &#37;&#125;
&#123;&#37; endfor &#37;&#125;
</code>
</pre>

This `liquid` template simply navigates through all the pages and add only those to the navigation menu which do not have any `slug`. Pretty neat. Thanks, [Kasper Isager](https://gist.github.com/kasperisager)!

{% highlight ruby linenos %}
    {% assign entries = site.pages | sort: "path" %}
{% endhighlight %}
