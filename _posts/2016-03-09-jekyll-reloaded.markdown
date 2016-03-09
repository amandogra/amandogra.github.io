---
layout: post
title: "Jekyll Reloaded"
date: 2016-03-09T11:59:00-08:00
---

I've been using jekyll for few months now. I like this framework because you can blog using markdown through ViM in your very own terminal (iTerm). I have a blog which I was (somewhat) mantaining at [amandogra.github.io](http://amandogra.github.io), but the problem with that blog was that I was not satisfied with the theme. I was a wonderful theme by crafted by [John Otander](http://johnotander.com/) ([@4lpine](https://twitter.com/4lpine)), but I wanted somthing with my stamp on it. Plus I also wanted to learn the hidden secrets of the awesome jekyll framework. 

## Getting rid of the current setup
To get rid of the current setup I did the following:
    1. Pulled the latest from amandogra.github.io [ repository ](https://github.com/amandogra/amandogra.github.io).
    2. Tool the backup of the posts, favicons and Apple icon files.
    3. Created a new branch and named it 'newdesign' (How creative, right?)
    4. Deleted everything which was there under amandogra.github.io directory.

## Installed fresh Jekyll
This is same as installing a new jekyll framework from scratch. More information could be found at [Jekyll's website](https://jekyllrb.com/). Four commands and you are up and running.

I then created a new jekyll scaffold in amandogra.github.io directory using the following command:

```
jekyll new .
```
This created a new jekyll folder structure inside amandogra.github.io directory. Nice and clean! I bumped the server by running the following command once:

```
jekyll serve
```
Loaded `localhost:4000` in my browser and checked that the clean new blog is there with default text and settings. Clean slate!

## Set the `_config.yml`
Set the basic things like 'Name' and 'url' in the config file. The initial settings in `_config.yml` file are as below:

```
# Site settings
title: Aman Dogra
email: amandogra@gmail.com
description: A single place to record all the progress I am trying to make or making in my projects
baseurl: "" # the subpath of your site, e.g. /blog
url: "http://amandogra.github.io" # the base hostname & protocol for your site

```

## Edited the Social Icons
Changed the social icons in the footer.html by using the guide from [Aleksandar Todorović](https://blog.r3bl.me/en/simple-social-media-links-jekyll/). Completely optional step, but I like socializing (online!).

## Installed 'octopress'
According to the 'Read Me' file on their repository, [Octopress](https://github.com/octopress/octopress) is an obsessively designed toolkit for writing and deploying Jekyll blogs. What it actually does is that it automates the process of creation of new posts and pages. With simple commands in the terminal the pages/posts files are created and named properly.

I installed it using the Installation guide in the repository. It is a simple command:

```
gem install octopress
```
As mentioned in the same 'Read Me' file, Octopress reads from the `_config.yml` for the default settings. So I updated the `_config.yml` with the following:

```
# Default extension for new posts and pages
post_ext: markdown
page_ext: html

# Default templates for posts and pages
# Found in _templates/
post_layout: post
page_layout: page

# Format titles with titlecase?
titlecase: true

# Change default template file (in _templates/)
post_template: post
page_template: page
draft_template: draft

```

## Created my first post
Installing octopress is totally optional. One can create a new post in jekyll by typing in the file names in proper format, but with experience I can tell that, one could easily mess the names and date formats up while creating a new post. Hence an automation script is a welcome.
After the octopress is installed, I ran the following command in my directory `amandogra.github.io`:

```
 octopress init .
```
This command added the Octopress scaffold. Now to create a new post I simply executed the following command:

```
octopress new post "Jekyll reloaded"
```
Voila! a new page was created under the `_posts` directory as `2016-03-09-jekyll-reloaded`
I opened that file in my favorite editor (ViM) and started typing in `markdown` format.

## Copy old posts
Now was the time to copy the old posts from the backup folder and put it into the `_posts` directory of the new setup.

## Check everything
I run the jekyll server using the `watch` switch so that I don't have to restart it each time I make any change to my files.
Send `Ctrl+c` signal if the jekyll server is already running. Execute the following command:

```
 jekyll serve --watch
```
Checked the localhost:4000 again and saw that all my posts are there.

Pushed the changes to github.

Now it was time for the installation of a new theme for jekyll which I am going to cover that in next post.
