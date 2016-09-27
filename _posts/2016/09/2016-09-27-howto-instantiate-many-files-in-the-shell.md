---
layout: "post"
title: "HOWTO: Instantiate many files in the shell"
date: "2016-09-27 17:44"
---

# Problem

Create these file with these contents:

Filename  | Contents  
::|::
A.txt  | Hello, I'm A
B.txt  | Hello, I'm B
C.txt  | Hello, I'm C
D.txt  | Hello, I'm D
E.txt  | Hello, I'm E

Notice the pattern, the file `${name}` are reused in the content, and the content seems to have this pattern: `Hello, I'm ${name}`

First let's gather the name into an array:

```
NAME=(A B C D E)
```

Then, a for loop to go through the names, then echo the pattern and pipe into a file with the name.

```
for name in ${NAME}; do
  echo "Hello, I'm ${name}" > ${name}.txt
done
```

This should solve the problem
