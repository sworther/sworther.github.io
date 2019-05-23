---
title: "Git"
date: 2018-07-27T15:55:59+08:00
draft: false
categories:
- cli
tags: [git]
---

# howto
- Git merge: accept theirs for multiple conflicts
```bash
git merge test-development
# Automatic merge failed, a bunch of conflicts!
git checkout --theirs ./path
git add ./path
git commit
```

- commit without message
```bash
git commit -a --allow-empty-message -m ''
```
