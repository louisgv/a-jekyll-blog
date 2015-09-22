---
layout: post
title: How long will JavaScript take to count to 9 Billion?
tagline: JavaScript - Profiling speed
date: '2015-09-22 00:52'
tags:
  - trick
categories:
  - javascript
---

# 57 seconds, or 56911ms

## Problem

A project is projected to be storing more than 10 billion data by next year. Measuring how intensive processing these data might give one a good picture of how they should prep.

## Planning

The algorithm used to measure interval consists of two data point: the `start` time and the `end` time, measured before and after a function's execution.

The `interval` is thus `end - start`

Time in JavaScript can be measured using the Date object.

## Product

```
var start = new Date().getTime();

//Any kind of function is here
for (i = 0; i < 10000000000; ++i) {}

var end = new Date().getTime();
var time = end - start;
console.log('Execution time: ' + time);

```
