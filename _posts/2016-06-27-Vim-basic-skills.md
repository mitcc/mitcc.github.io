---
layout: post
title: Vim Basic Skills
date: 2016-06-27 22:55:08
permalink: vim-basic-skills
disqus: y
---

* delete

|Command   |Explanation|
|---------:|:----------------|
|:ndk      |delete current and n lines above. (n + 1 lines in total)|
|:g/^$/d   |delete all empty lines|
|:g/^\s*$/d|delete all lines that are empty or that contain only whitespace characters (spaces, tabs)|

* yank

|Command|Explanation|
|------:|:----------------|
|y$     |yank to the end of the current line (but don't yank the newline character)|
|^y$    |the current line (but don't yank the newline character)|


* case change

|Command|Explanation|
|------:|:----------------|
|~      |Toggle case of the character under the cursor, or all visually-selected characters|
|3~     |toggle case of the next three characters|
|g~     |toggle case change|g~ig~iww
|g~3w   |toggle case of the next three words|
|g~iw   |toggle case of the current word (inner word – cursor anywhere in word)|
|g~$    |toggle case of all characters to end of line|
|g~~    |toggle case of the current line (same as V~)|
|gu     |toggle lowercase|
|gU     |toggle uppercase|
|guu    |change the current line to lowercase (same as vu)|
|gUU    |change the current line to uppercase (same as VU)|
|gUiw   |change current word to uppercase|


