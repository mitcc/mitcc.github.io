---
layout: post
title: Bitwise Skills
date: 2016-07-04 15:26:25
permalink: Bitwise-Skills
disqus: y
---

==========

```Java
    /**
     * Returns a power of two size for the given target capacity.
     */
    static final int tableSizeFor(int cap) {
        int n = cap - 1;
        n |= n >>> 1;
        n |= n >>> 2;
        n |= n >>> 4;
        n |= n >>> 8;
        n |= n >>> 16;
        return (n < 0) ? 1 : (n >= MAXIMUM_CAPACITY) ? MAXIMUM_CAPACITY : n + 1;
    }
```

这是HashMap(Java) 源代码中的一个方法
