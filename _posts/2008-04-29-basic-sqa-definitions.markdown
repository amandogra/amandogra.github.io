---
layout: post
title: 'Basic SQA Definitions'
date: 2008-04-29 02:52:00.000000000 -07:00
type: post
published: true
status: publish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra
  blogger_5b414faa76516d87e0b4b243ad1d0e3b_permalink: '2002950109822567058'
author: aman Dogra
---

Very Strangely, I woke up early in the morning at around 6:15 AM. They
say mind is fresh in the morning. My mind was so fresh, that I was
having hard time deciding that what should I read? As I am a bit ill for
few days, I was preferring not to look at the computer screen, so I
decided to study something from a book. 

<!--more-->

Moreover, I was reading Pressman's Testing book yester-night, so I decided to study the same chapter 'Testing Strategies'. Today I learnt the definitive difference
between Unit, Integration, and Regression Testing. Actually, I am not a
person who is good at definitions, but Tarn invoked me yesterday by
asking some definitions related to SQA, so here is it now:

*Unit Testing* focuses verification effort on the smallest unit of
software design - The software component or module. Unit Testing is
usually adjunct to the coding step. Mostly, unit testing is done by the
developer who is developing the software module. The developer uses
drivers or stubs to input data (for data flow) to the module. Boundary
testing is one of the most important part of the unit testing tasks.

*Integration Testing* is performed whenever a new module is added to an
already (unit) tested module. The main purpose of the integration
testing could be explained in one line as 'These two modules are working
independently. Now test are they working correctly if we put them
together. The integration testing could be performed in increments. It
is known as incremental integration testing. I'll explain 'Incremental
Integration Testing' in next post.

*Regression Testing* is re-executing some subset of tests that have already been conducted to ensure that changes have not propagated unintended side effects. Each
time a new module is added as part of integration, the software changes,
some new data paths are established and thus some problems may surface
which are unattended. Regression Testing is done as a
go-through-the-software process just to ensure that the changes have not
propagated unattended side-effects.

A very good reference for those who are interested in Software Testing
is <http://amit-badola.blogspot.com/>. This blog contains simple and
precise explanations of the things related to SQA
