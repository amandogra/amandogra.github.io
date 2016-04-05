---
layout: article
title: Finding which process is holding the port
date: 2010-10-28 16:13:00.000000000 -07:00
type: post
categories: blog
published: true
status: publish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra Aman Dogra
  first_name: ''
  last_name: ''
---

This issue kept me stuck for about 6 straight hours, so I assume, that it is my moral duty to record it down in my blog. The issue was like this. When I was restarting (or starting) my apache server, I was getting an error like "unable to bind 0.0.0.0:80 address"
<!--more-->

I know some of you would find it quite silly, but there might be some
people who still be struggling with this issue.

Well, I am using Ubuntu9.04 with the default apache2. This issue could
occur due to many of the reasons, but in my case the port 80 was not
free. So to find what is binding the port run the following command:\

```
sudo netstat -antlp | grep :80
```

This will display a list of processes working on port 80 in a tabular
format. The last column in the table is the PID or Process ID.

Run the following command to kill this process\

```
sudo kill -9 1234 
```

(Be sure to replace the number 1234 with the actual PID)

If there are more processes then repeat this command with those
processes IDs also

Thats it! try restarting the apache server now.
