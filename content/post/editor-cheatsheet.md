---
title: "editor Cheatsheet"
date: 2018-07-25T01:11:54+08:00
draft: false
categories: ["tool"]
tags: ["cheatsheet"]
hiddenFromHomePage: true
---


# vim ex command pattern 
```python
# Text Processing Commands
- : [ range ] command [ args ... ]

# Search and Replace
- :[range]s/pattern/replacement[/flags...]

# Global Actions
- :[range]g/pattern/command


# All-Purpose Filter
:range!command
```

-  How do i insert a blank line before every comment (eg “#”) in VIM?
```
:g/^#/norm O
```
    This is a shortcut of `:global/^#/normal O` which means:

    - for each line starting with '#' `(:global/^#/)`
    - do 'O' command in 'normal mode' (normal O) – which means to do what a 'O' key does in the 'normal' (not insert and not :command) VIM mode. And 'O' inserts a new line.


# markdown 引用时候怎么换行

> 隐约雷鸣 阴霾天空
但盼风雨来 能留你在此
隐约雷鸣 阴霾天空
即使天无雨. 我亦留此地。  

每行后面加两个空格，即换行用空格空格回车。

> 隐约雷鸣 阴霾天空   
但盼风雨来 能留你在此   
隐约雷鸣 阴霾天空   
即使天无雨. 我亦留此地。  