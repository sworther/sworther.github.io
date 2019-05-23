---
title: "Python Iterator"
date: 2018-08-02T16:39:32+08:00
lastmod: 2018-08-02T16:39:32+08:00
draft: false
categories: [python]
tags: [iterator generator]
keywords: []
description: ""
---


# concept
## generator vs iterator
Every generator is an iterator, but not vice versa

## itarator vs itarable
- Iterable的__iter__方法会返回一个Iterator, Iterator的__next__方法（Python 2里是next）会返回下一个迭代对象，如果迭代结束则抛出StopIteration异常。

- Iterator自己也是一种Iterable，所以也需要实现Iterable的接口，也就是__iter__，这样在for当中两者都可以使用。Iterator的__iter__只需要返回自己就行了。

## generator class
```python

class Fib:
    def __init__(self):
        self.a, self.b = 0, 1
    def __iter__(self):
        while True:
            yield self.a
            self.a, self.b = self.b, self.a+self.b

f = iter(Fib())
for i in range(3):
    print(next(f))


class Fib:
    def __init__(self):
        self.a, self.b = 0, 1        
    def __next__(self):
        return_value = self.a
        self.a, self.b = self.b, self.a+self.b
        return return_value
    def __iter__(self):
        return self

f = iter(Fib())
for i in range(3):
    print(next(f))
```

