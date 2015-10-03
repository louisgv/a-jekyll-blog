---
layout: post
title: 'Socket.io, and scale...'
date: '2015-10-02 19:14'
tags:
  - counter
categories:
  - big-problem
---

# Problem:
Big Countdown

## Elaborate:
  A service that handle a big number of request per instant of time. For each request reduce the number by an unit.

# Method:
## Vertical Scalling
  + Client emit signal for server to handle the Countdown
  + This method requires the technology used be scalable.
  + Redis + Socket.io: Does the event emit good for this? Can this scale really big? IF so, we can just use this method.

## Distributed counting
  + Each client instance count for itself, then merged at a certain instance of time.
  + This method requires a management system that allocates as well as synchronize the count
