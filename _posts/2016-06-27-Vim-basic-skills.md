---
layout: post
title: Vim Basic Skills
date: 2016-06-27 22:55:08
permalink: Vim-Basic-Skills
disqus: y
---

*  delete current and n lines above. (n + 1 lines in total)

####  Syntax:

####  :ndk

####  Example: 

####  :3dk

* delete all empty lines

#### :g/^$/d

* delete all lines that are empty or that contain only whitespace characters (spaces, tabs)

####  :g/^\s*$/d

####  y$
* yank to the end of the current line (but don't yank the newline character);

####  ^y$
* the current line (but don't yank the newline character);

