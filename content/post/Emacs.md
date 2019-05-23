---
title: Emacs
date: 2017-10-05 21:46:45
categories:
- tool
tags:
- spacemacs 
- iedit
- emacs-info
---

# info system 
eg :What is the difference between setq and defvar in Emacs lisp?

- `C-h i`, 
- `m Elisp` choose the Elisp manual
- `i defvar` search the index for "defvar"
That's all

## lexical binding(scope)
elisp默认是dynamical scope, 若想使用statical binding,可以通过`(setq lexical-binding t)`或者elisp文件头部加上
```elisp
;;-*- lexical-binding: t -*- 
```  

# gdb in emacs
M-x gdb
- toggle gdb frame
M-x gdb-many-wondows

## gdb python-interactive 退出
- Ctrl-D evil下没用
- comint-send-eof
- gdb-io-eof

## 调试多个程序，gud-gdb， gdb 不支持。

## gdb IO
gdb 需要输入时，跳转到inferior I/O buffer,输入。  gud-gdb直接在gud buffer输入。 


# start with another init file
- alias emacs='emacs -q --load "/path/to/init.el"'
    - emacs -q -l ~/my-init-file.el

- env HOME=/path/to/dir emacs
    You then use /path/to/dir/.emacs.d

# magit
magit status 快捷键： `SPC g s`
magit dispatch 快捷键： `SPC g m`

# iedit
- spacemacs 中的 muiti cursors 实现
快捷键： `SPC s e`
tips
 - 配合`SPC n r`可以进行区域选定。
 - F 则是函数体范围选定。

# helm-ag
`SPC s s`
`C-c C-e`  helm swoop edit buffer

# c-c++ layer
## clang support 补全问题
按教程设置之后，仍不能自动补全，经一番查找之后，发现是没有设置工程目录的.clang_complete,不过应该是逐级向上查找的。所以设置在home目录最好。
```
-I/usr/include/c++/7/
``` 
# yas-snippets
- auto completion 
- `C-p` | `M-/` yas-hippie-try-expand  hippie expand

# winum number don't start with 1 in new frame when in emacs client
- in user-config 
(setq winum-scope 'frame-local)
