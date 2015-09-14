---
layout: post
title: Ionic w/ Sass
tagline: node 4.0.0
date: '2015-09-14 07:35'
tags:
  - ionic
  - nodejs
categories:
  - tip n trick
---

So node just swallowed io.js and now morphed into version 4.0.0. Upgrade the boy is cool and all, but ionic project will start to fire crappy error. This blog will be updated as I stumble upon more errors with sass.

# ionic setup sass

This command yield this annoying error

```
/home/lab/pro/louisgv.github.io/dev/node_modules/gulp-sass/node_modules/node-sass/lib/index.js:22
    throw new Error('`libsass` bindings not found. Try reinstalling `node-sass`?');
    ^

Error: `libsass` bindings not found. Try reinstalling `node-sass`?
    at getBinding (/home/lab/pro/louisgv.github.io/dev/node_modules/gulp-sass/node_modules/node-sass/lib/index.js:22:11)
    at Object.<anonymous> (/home/lab/pro/louisgv.github.io/dev/node_modules/gulp-sass/node_modules/node-sass/lib/index.js:188:23)
    at Module._compile (module.js:434:26)
    at Object.Module._extensions..js (module.js:452:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Module.require (module.js:365:17)
    at require (module.js:384:17)
    at Object.<anonymous> (/home/lab/pro/louisgv.github.io/dev/node_modules/gulp-sass/index.js:3:17)
    at Module._compile (module.js:434:26)

Error running gulp sass
```

Basically, gulp sass failed, no more styling! The issue is boiled down to deprecated middle-wares which were compiled using an older version of the C library packed with the previous Node. To solve this issues, first in your project directory run `rm -rf node_modules` to remove all local node modules.

Now to kill the sass problem, run `npm install gulp-sass --save-dev`, which hopefully will install the correct version of sass and node-sass.

Lastly, do `npm install` to re-install the node_modules folder with the new node.

Now `ionic setup sass` should run smoothly and say

```
Successful sass build
Ionic setup complete
```
