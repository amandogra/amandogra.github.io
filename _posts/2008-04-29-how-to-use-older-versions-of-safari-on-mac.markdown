---
layout: post
title: 'How to use Older versions of Safari on Mac'
date: 2008-04-29 10:24:00.000000000 -07:00
type: post
published: true
status: publish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra
  blogger_5b414faa76516d87e0b4b243ad1d0e3b_permalink: '1099120545366733969'
author: Aman Dogra
---

For some testing purpose I needed Safari 2.0 on Mac OS X 10.4
\[Tiger\] as well as Mac OS X 10.5 \[Leopard\]. Few links which I felt
are really helpful are:

<http://michelf.com/projects/multi-safari/> - This link contains a number
of old versions of Safari

<http://tripledoubleyou.subtlegradient.com/stuff/Safari2/> - This link
provides the method to install the Safari 2.0 on Mac 10.5 Leopard.

<!--more-->

I am just copying it down for backup purpose:

1. Download the zip — Safari 2.0.4.zip

2. Unzip the zip

3. Drag Safari 2.0.1 into your Applications folder

4. Wipe your LaunchServices cache by executing following command in
Terminal:
`
    /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/LaunchServices.framework/Versions/A/Support/lsregister -kill -r -domain local -domain system -domain user
`

5. Enable the Debug Menu in your new Safari 2 by executing following
command in Terminal:
`
    defaults write com.apple.Safari.MultiSafari204 IncludeDebugMenu 1
`

6. Launch Safari 2.0.1
