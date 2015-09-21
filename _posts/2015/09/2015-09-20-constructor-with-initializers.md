---
layout: post
title: "Constructor with Initializers"
date: "2015-09-20 13:41"
---


```
  var Girl = function(iName, iAge, iIsCute, iDance){
    this.info = {
      name : iName,
      age : iAge,
      isCute: iIsCute,
    };

    this.dance = iDance;

    this.log = this.info.name + " is " + this.info.age + " years old";
  }

  var vivi = new Girl ("Vivi", 17, true, function(){
      console.log("Wiggle");
  });

  var elena = new Girl ("Elena", 21, true, function(){
      console.log("Disco");
  });

```
