---
layout: post
title: Vim Basic Skills
date: 2016-06-27 22:55:08
permalink: vim-basic-skills
disqus: y
---



* replace
|Command|Explanation|
|:-----:|:----------|
|<kbd>r</kbd>|replace character under current cursor| 
|<kbd>R</kbd>|replace from current cursor| 

* move

|Command|Explanation|
|:-----:|:----------------|
|<kbd>n</kbd><kbd>\|</kbd>|move cusor to the column of n|

* delete

|Command   |Explanation|
|:--------:|:----------------|
|<kbd>:</kbd><kbd>n</kbd><kbd>d</kbd><kbd>k</kbd>|delete current and n lines above. (n + 1 lines in total)|
|<kbd>:</kbd><kbd>g</kbd><kbd>/</kbd><kbd>^</kbd><kbd>$</kbd><kbd>/</kbd><kbd>d</kbd>|delete all empty lines|
|<kbd>:</kbd><kbd>g</kbd><kbd>/</kbd><kbd>^</kbd><kbd>\\</kbd><kbd>s</kbd><kbd>*</kbd><kbd>$</kbd><kbd>/</kbd><kbd>d</kbd>|delete all lines that are empty or that contain only whitespace characters (spaces, tabs)|

* yank

|Command|Explanation|
|:-----:|:----------------|
|<kbd>y</kbd><kbd>$</kbd>|yank to the end of the current line (but don't yank the newline character)|
|<kbd>^</kbd><kbd>y</kbd><kbd>$</kbd>|the current line (but don't yank the newline character)|


* case change

|Command|Explanation|
|:-----:|:----------------|
|<kbd>~</kbd>|toggle case of the character under the cursor, or all visually-selected characters|
|<kbd>3</kbd><kbd>~</kbd>|toggle case of the next three characters|
|<kbd>g</kbd><kbd>~</kbd>|toggle case change|
|<kbd>g</kbd><kbd>~</kbd><kbd>3</kbd><kbd>w</kbd>|toggle case of the next three words|
|<kbd>g</kbd><kbd>~</kbd><kbd>i</kbd><kbd>w</kbd>|toggle case of the current word (inner word – cursor anywhere in word)|
|<kbd>g</kbd><kbd>~</kbd><kbd>$</kbd>|toggle case of all characters to end of line|
|<kbd>g</kbd><kbd>~</kbd><kbd>~</kbd>|toggle case of the current line (same as V~)|
|<kbd>g</kbd><kbd>u</kbd>|toggle lowercase|
|<kbd>g</kbd><kbd>U</kbd>|toggle uppercase|
|<kbd>g</kbd><kbd>u</kbd><kbd>u</kbd>|change the current line to lowercase (same as vu)|
|<kbd>g</kbd><kbd>U</kbd><kbd>U</kbd>|change the current line to uppercase (same as VU)|
|<kbd>g</kbd><kbd>U</kbd><kbd>i</kbd><kbd>w</kbd>|change current word to uppercase|

* split window

|Command|Explanation|
|:-----:|:----------------|
|<kbd>:</kbd><kbd>s</kbd><kbd>p</kbd> or <kbd>Ctrl</kbd><kbd>w</kbd><kbd>s</kbd>|split the current window horizontally, loading the same file in the new window|
|<kbd>:</kbd><kbd>v</kbd><kbd>s</kbd><kbd>p</kbd> or <kbd>Ctrl</kbd><kbd>w</kbd><kbd>v</kbd>|split the current window vertically, loading the same file in the new window|
|<kbd>:</kbd><kbd>q</kbd>|close the currently active window|
|<kbd>:</kbd><kbd>o</kbd><kbd>n</kbd>|close all windows except the currently active window|
