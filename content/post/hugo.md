---
title: "Hugo"
date: 2018-07-27T16:12:41+08:00
draft: true
categories: [cli]
tags: [hugo]

hiddenFromHomePage: true
---

- 部署命令
  ```bash


alias gcn!='git commit -v --no-edit --amend'
alias gpf!='git push --force'
alias gcan!='git commit -v -a --no-edit --amend'


alias blog='cd  /d/gh-pages/li-hugo && cd content && git add -A && gcan! && gpf! && cd .. && hugo && cd public && git add -A && gcn! && gpf! ' 

alias blog!='cd  /d/gh-pages/li-hugo && cd content && git add -A && gcan! && gpf! && cd .. && hugo && cd public && git add -A && gcn! && gpf! && cd  "/c/Program Files (x86)/Google/Chrome/Application"  && ./chrome "https://gitee.com/sworther/sworther/pages"' 
  ```
