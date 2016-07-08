---
layout: post
title: Vim Basic Skills
date: 2016-06-27 22:55:08
permalink: vim-basic-skills
disqus: y
---


####  :ndk
*  delete current and n lines above. (n + 1 lines in total)

* delete all empty lines

#### :g/^$/d

* delete all lines that are empty or that contain only whitespace characters (spaces, tabs)

####  :g/^\s*$/d

####  y$
* yank to the end of the current line (but don't yank the newline character);

####  ^y$
* the current line (but don't yank the newline character);

-------------------

* case change

|Command|Explanation       |
|-------|------------------|
|g~     |toggle case change|
|gu     |toggle lowercase  |
|gU     |toggle uppercase  |


