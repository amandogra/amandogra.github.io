---
layout: article
title: 'How to copy a file from remote mac or *nix using SSH'
date: 2008-06-05 11:44:00.000000000 -07:00
type: post
categories: blog
published: true
status: publish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra
  blogger_5b414faa76516d87e0b4b243ad1d0e3b_permalink: '629151710482891841'
author: Aman Dogra
---

There are times when you are working on a remote linux or mac
machine and you have to copy a file to your own \*nix or mac machine.
So, Tarun told me a way for that today. I am going to explain this with
the help of an example. I am assuming that both the remote and the local
machine are using mac OS.

<!--more-->

Suppose the IP of remote mac machine is 192.168.1.1 and the IP of your
local machine is 192.168.1.2. The directory which you want to copy is
located at /Users/remote/copyMe/ and the location where you want to
place it on your machine is /Users/local/placeHere/ \[sidenote: to find
the IP of your machine. Run the Terminal and type `ifconfig`\] 
Now Open the Terminal on your local machine and type:

```
ssh [remote_ip_address] -l [remote_user_name]

e.g., ssh 192.168.1.1 -l root
```

Note here that it is small L (not one) switch after the remote address
and that the remote_user_name is the username to access the remote
machine

With this command you'll be asked for the login password. Once the
correct password is filled you will be able to enter the remote machine.
Now is the time to copy the directory \[or just a file\] from this
remote machine to your local machine. This can be done in a single
command. Like this:

```
scp -r [path to the source]
[local_user_name]@[local_ip_address]:[path to the destination]
```

Now let me make it non-generic

```
scp -r /Users/remote/copyMe/ aman@192.168.1.2:/Users/local/placeHere/
```

Now all the contents of the remote directory 'copyMe', will be placed
under 'placeHere' local directory. I have used a -r here to copy the
directory recursively. if you are copying only a file then there is no
need for this switch.

So was that so difficult? ;)
