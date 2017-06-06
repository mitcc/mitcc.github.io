---
title: Vim Basic Skills
date: 2016-06-27 22:55:08
---



# replace

|Command|Explanation|
|:-----:|:----------|
|:%s/\\(.\*\\)/something\1|get the whole line and replace, \1 is the content of the line, for examle :%s/\\(.\*\\)/String \1 = "";|
|r|replace character under current cursor| 
|R|replace from current cursor| 
|:%s/$/xxx/ 或者 :x,ynorm Axxx<kbd>Esc<\/kbd>|每行的行尾添加相同的内容"xxx"|
|:%s/xxx.\*/yyy/|从xxx处至行尾替换成yyy,其中若"yyy"为空串，则可变为从"xxx"处删至行尾|
|:g/red/s/blue/green|替换包含某字符串的行,to replace "blue" with "green" in lines that contain "red"|
|:g!/red/s/blue/green|替换不包含某字符串的行,to do the replacement in lines that do not contain "red"|
|%s/^)/somestring/|替换以)开头的行, /^)查找以)开头的行,在查找的内容前加上**^**|
|:%s/\cmyString/newString/g|查找、替换时不区分大小写,在查找的内容前加上**\c**|

# delete

|Command   |Explanation|
|:--------:|:----------------|
|:%norm f:D|对每一行删除冒号及冒号之后的内容,其中f前可加上数字1，表示从第几个冒号开始删除，若D前加上小写字母"l(L)",则删除内容不包括冒号|
|:ndk|delete current and n lines above. (n + 1 lines in total)|
|:%s/^.\*+//|删除一行中+前的内容，包含+|
|:s/^.\*\(FOO\)/\1/|删除一行中FOO前的内容，不包含FOO|
|:%s/.\*Hello/Hello/|删除最后一个匹配的Hello之前的内容|
|:%s/.\\{-}Hello/Hello|删除第一个匹配的Hello之前的内容|
|df#|从光标处删至#符号(包含)|
|dF#|从光标处反向删至#符号(包含)|
|dt#|从光标处删至#符号(不包含)|
|dT#|从光标处反向删至#符号(不包含)|
|d^|从光标处删至行首|
|dgg|从当前行删至首行|
|d$|从光标处删至行尾|
|dG|从当前行删至尾行|
|ggdG|删除所有行|
|:%d|删除所有行|
|:1,$d|删除所有行|
|:g/.\*/d|删除所有行|
|:g/^$/d|delete all empty lines|
|:g/^\\s\*$/d|delete all lines that are empty or that contain only whitespace characters (spaces, tabs)|
|:g/abcd/d|删除所有包含"abcd"的行|
|:%g!/abcd/d|删除所有不包含"abcd"的行|
|:%g!/abcd\\\|efgh/d|删除所有不包含"abcd"且不包含"efgh"的行|
|3dk|删除当前及上面3行，即一共3+1行|
|3dd|向下删除,一共3行|
|dip|删除整段|
|dap|删除整段|
|diw|删除一个单词|
|daw|删除一个单词|

# yank

|Command|Explanation|
|:-----:|:----------------|
|y$|yank to the end of the current line (but don't yank the newline character)|
|^y$|the current line (but don't yank the newline character)|
|y5l|向后复制5个字符|
|y5h|向前复制5个字符|
|:4co.<kbd>Enter</kbd>|复制第4行并粘贴至当前行的下一行|
|:xcoy<kbd>Enter</kbd>|复制第x行并粘贴至y行的下一行|
|yip|复制整段|
|yap|复制整段|
|yip|复制一个单词|
|yap|复制一个单词|

# count

|Command|Explanation|
|:-----:|:----------------|
|:%s/string//gn|统计某匹配串出现的次数|

# search

|Command|Explanation|
|:-----:|:----------|
|\*|search for the word under the cursor forward|
|#|search for the word under the cursor backward|

# move

|Command|Explanation|
|:-----:|:----------------|
|n\||move cusor to the column of n|

# highlight settings

|Command|Explanation|
|:-----:|:----------------|
|:noh|取消替换、搜索之后的高亮|

# case change

|Command|Explanation|
|:-----:|:----------------|
|~|toggle case of the character under the cursor, or all visually-selected characters|
|3~|toggle case of the next three characters|
|g~|toggle case change|
|g~3w|toggle case of the next three words|
|g~iw|toggle case of the current word (inner word – cursor anywhere in word)|
|g~$|toggle case of all characters to end of line|
|g~~|toggle case of the current line (same as V~)|
|gu|toggle lowercase|
|gU|toggle uppercase|
|guu|change the current line to lowercase (same as vu)|
|gUU|change the current line to uppercase (same as VU)|
|gUiw|change current word to uppercase|

# split window

|Command|Explanation|
|:-----:|:----------------|
|:sp or Ctrl+w+s|split the current window horizontally, loading the same file in the new window|
|:vsp or Ctrl+w+v|split the current window vertically, loading the same file in the new window|
|:q|close the currently active window|
|:on|close all windows except the currently active window|
