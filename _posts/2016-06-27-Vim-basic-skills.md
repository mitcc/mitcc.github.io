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
|<kbd>:</kbd><kbd>%</kbd><kbd>s</kbd><kbd>/</kbd><kbd>\\</kbd><kbd>(</kbd><kbd>.</kbd><kbd>*</kbd><kbd>\\</kbd><kbd>)</kbd><kbd>/</kbd><kbd>somestring</kbd><kbd>\\</kbd><kbd>1</kbd>|get the whole line and replace, \1 is the content of the line, for examle <kbd>:%s/\(.*\)/String \1 = "";</kbd>|
|<kbd>r</kbd>|replace character under current cursor| 
|<kbd>R</kbd>|replace from current cursor| 
|:%s/$/XXX/|每行的行尾添加相同的内容"XXX"|
|:%s/XXX.*/YYY/|从XXX处至行尾替换成YYY,其中若"YYY"为空串，则可变为从"XXX"处删至行尾|
|:g/red/s/blue/green|替换包含某字符串的行,to replace "blue" with "green" in lines that contain "red"|
|:g!/red/s/blue/green|替换不包含某字符串的行,to do the replacement in lines that do not contain "red"|

* delete

|Command   |Explanation|
|:--------:|:----------------|
|<kbd>:</kbd><kbd>%</kbd><kbd>n</kbd><kbd>o</kbd><kbd>r</kbd><kbd>m</kbd><kbd>Space</kbd><kbd>f</kbd><kbd>:</kbd><kbd>D</kbd>|对每一行删除冒号及冒号之后的内容,其中f前可加上数字1，表示从第几个冒号开始删除，若D前加上小写字母"l(L)",则删除内容不包括冒号|
|<kbd>:</kbd><kbd>n</kbd><kbd>d</kbd><kbd>k</kbd>|delete current and n lines above. (n + 1 lines in total)|
|<kbd>:</kbd><kbd>g</kbd><kbd>/</kbd><kbd>^</kbd><kbd>$</kbd><kbd>/</kbd><kbd>d</kbd>|delete all empty lines|
|<kbd>:</kbd><kbd>g</kbd><kbd>/</kbd><kbd>^</kbd><kbd>\\</kbd><kbd>s</kbd><kbd>*</kbd><kbd>$</kbd><kbd>/</kbd><kbd>d</kbd>|delete all lines that are empty or that contain only whitespace characters (spaces, tabs)|
|:%s/^.*+//|删除一行中+前的内容，包含+|
|:s/^.*\(FOO\)/\1/|删除一行中FOO前的内容，不包含FOO|
|:%s/.*Hello/Hello/|删除最后一个匹配的Hello之前的内容|
|:%s/.\{-}Hello/Hello|删除第一个匹配的Hello之前的内容|
|df#|从光标处删至#符号(包含)|
|dt#|从光标处删至#符号(不包含)|
|dgg|从当前行删至首行|
|dG|从当前行删至尾行|
|ggdG|删除所有行|
|:%d|删除所有行|
|:1,$d|删除所有行|
|:g/.*/d|删除所有行|

* yank

|Command|Explanation|
|:-----:|:----------------|
|<kbd>y</kbd><kbd>$</kbd>|yank to the end of the current line (but don't yank the newline character)|
|<kbd>^</kbd><kbd>y</kbd><kbd>$</kbd>|the current line (but don't yank the newline character)|
|y5l|向后复制5个字符|
|y5h|向前复制5个字符|

* move

|Command|Explanation|
|:-----:|:----------------|
|<kbd>n</kbd><kbd>\|</kbd>|move cusor to the column of n|

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
