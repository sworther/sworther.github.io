---
title: cli cheatsheet
date: 2017-12-11 17:25:41
categories: ["cli"]
tags:
- sed
- re
- tmux
---

# sed
- Matched string notation (&)
```sh
echo this is an example | sed 's/\w\+/[&]/g'
```
- Substring match notation (\1)
```bash
echo this is digit 7 in a number | sed 's/digit \([0-9]\)/\1/'
this is 7 in a number
```

- \b usage (b: word boundary marker)
```bash
cat sed_data.txt
11 abc 111 this 9 file contains 111 11 88 numbers 0000
```
```bash
sed -i 's/\b[0-9]\{3\}\b/NUMBER/g' sed_data.txt
```
```bash
cat sed_data.txt
11 abc NUMBER this 9 file contains NUMBER 11 88 numbers 0000
```


# regular expression
```bash
'\d+(?=\.\w+$)'

file4.txt will match 4.
file123.txt will match 123.
demo.3.js will match 3 and so on.

difference between ?:, ?! and ?= in regex?

?: Match expression but do not capture it.
?= Match a suffix but exclude it from capture.
?! Match if suffix is absent.
```


# gdb
-q   quiet mode, Do not print the introductory and copyright messages.

# tmux pane sync
- turn on
`Ctrl-b` then ":set synchronize-panes"
- turn off:
`Ctrl-b` then ":setw synchronize-panes off"
### shortcut
bind e setw synchronize-panes on
bind E setw synchronize-panes off
### toggle shortcut
bind a set-window-option synchronize-panes
