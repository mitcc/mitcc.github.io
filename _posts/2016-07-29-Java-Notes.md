---
layout: post
title: Java学习笔记
date: 2016-07-29 00:53:47
permalink: java-notes
disqus: y
---



Java Arrays类源代码中的fill方法，使得**数组中的每个元素，均指向填入的同一个对象，而非将val复制a.length个，分别指向这些对象**，由下面的源代码很容易看出这点。

```
public class Arrays {

    public static void fill(Object[] a, Object val) {
        for (int i = 0, len = a.length; i < len; i++)
            a[i] = val;
    }

}
```
