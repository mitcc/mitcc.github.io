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

    /*
     * 省略其它成员变量、方法等
     */

    public static void fill(Object[] a, Object val) {
        for (int i = 0, len = a.length; i < len; i++)
            a[i] = val;
    }

}
```

Math类中的abs方法，返回值跟输入值的类型有关

```java
public static int abs(int a) {
    return (a < 0) ? -a : a;
}

public static long abs(long a) {
    return (a < 0) ? -a : a;
}

public static float abs(float a) {
    return (a <= 0.0F) ? 0.0F - a : a;
}

public static double abs(double a) {
    return (a <= 0.0D) ? 0.0D - a : a;
}
```