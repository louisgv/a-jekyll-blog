---
layout: post
title: "JS - Profile function speed"
date: "2015-09-20 16:38"
---

```
var start = new Date().getTime();

for (i = 0; i < 10000000000; ++i) {
// do something
}

var end = new Date().getTime();
var time = end - start;
alert('Execution time: ' + time);

```
