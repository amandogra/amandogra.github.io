---
layout: post
title: How to host MEAN stack app on Digital Ocean
date: 2015-10-04 15:59:55.000000000 -07:00
type: post
published: true
status: publish
categories:
tags:
meta:
author: Aman Dogra
---

In this post we are going to setup a working MEAN stack application on a
Digital Ocean virtual server from stratch. <!--more-->

Digital Ocean account
---------------------

First step first, go to [Digital Ocean](https://www.digitalocean.com/)
and sign up.

Create a droplet
----------------

Once you have created your account on Digital Ocean, go ahead and click
on ‘Create Droplet’ button on the top of the page.

You’ll be presented with different pricing options. Choose the ‘size’ as
per your requirements. I chose the first (least expensive) one. You
could upgrade anytime so feel free to choose anyone.

Under the “Select Region”, select a region which is near to your target
audience or you.

Under the “Select Image” section, there is a tab named “Distribution”.
Choose ‘Ubunut’ (latest version) here and from the ‘Applications’ tab
choose “Mean on ”

Fill in the billing information and you are presented with a new machine
of yours own.


Access Console
--------------

Now that you have a virtual machine setup, you should access it. So from
the top menu click on ‘Droplets’ and you’ll be presented with the list
of your droplets.

Click on the name of the droplet you just created.

On the next page, click on ‘Reset password’. You’ll get an email with a
temporary password.

On the page where you clicked on ‘Reset passowrd’, there is another
button names ‘Console Access’. Click on that and you’ll land on a
terminal. This is the face of your droplet.

Login as ‘root’ using the password you got in the email. Reset the
password as soon as you login. The system will ask you to do it
automatically.

Verify/Install MEAN
-------------------

After login, try to run the following command:

``` {.highlight}
 npm -version
```

If it returns with a proper version of NPM then that means that node is
installed already. You remember we chose MEAN in the applications tab
while creating droplet.

I have observed that MongoDB is not install by default. I might be wrong
but I used the following tutorial to install the MongoDB on Ubuntu14.04

[How to install MongoDB on Ubuntu
14.04](https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-14-04)


Install tmux (Optional)
-----------------------

Personally, for me, working on a single terminal was a bit difficult, so
I installed tmux on my droplet.

To do so, type the following command:

``` {.highlight}
 sudo apt-get install tmux
```

Once the tmux is installed take a crash course on tmux
[here](https://robots.thoughtbot.com/a-tmux-crash-course)


Clone your project
------------------

Now that our machine is set, we should concentrate on our project.
Download your project from github. If your project is not on github, I
would strongly advice you to do so. If you can not or don’t want to,
then you could SSH to your machine and copy the code through that to
your droplet.

If you don’t want to setup ssh, then while cloning the project from the
github pass the https url.


Process Management
------------------

Install [PM2](http://pm2.keymetrics.io/) and run your server using this
process manager. PM2 is a process manager which gives you a lot of
options.

You are all set. Check your application online using the IP Address
provided at the bottom of the console access page.

Feel free to contact me at amandogra@gmail.com, if you have any
questions regarding this post
