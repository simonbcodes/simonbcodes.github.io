---
layout: post
title: python tips
categories:
- python
- tutorial
---

This post is a compilation of small Python tips I've gotten used to using over the years. They're in no particular order, but feel free to try any that you don't know about.

### Underscore

In certain situations, you may not want to use a variable provided to you by some expression (this happens commonly with `enumerate` and looping). In this case, just replace the unneeded variable with `_`.

```python

fruits = ['apple', 'orange', 'lemon']

for i, _ in enumerate(fruits): # ignoring the value output for enumerate()
    print(i)

```

This is a relatively basic example, but its worth knowing about for some more obscure applications.

### Fast Swapping

Swapping the values of two variables comes up fairly often (especially in sorting algorithms). In most other languages, this swap would look something like this:

```python

a = [1, 2, 3]

tmp = a[0]
a[0] = a[1]
a[1] = tmp

```

Python provides a cleaner way of doing this via unpacking values:

```python

a = [1, 2, 3]

a[0], a[1] = a[1], a[0]

```

Much nicer, isn't it?
