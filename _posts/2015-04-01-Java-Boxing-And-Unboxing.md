---
layout: post
title: Java装箱与拆箱
date: 2015-04-01 14:21:25
permalink: java-boxing-and-unboxing
disqus: y
---

```java
public class Test {

    public static void main(String[] args) {
        for (int i = -130; i <= 130; i++) {
            Integer a = i;
            Integer b = i;
            System.out.println("i = " + i + ", a == b is: " + (a == b));

            /*
            java上面的输出结果为：
            i = -130, a == b is: false
            i = -129, a == b is: false
            i = -128, a == b is: true
            i = -127, a == b is: true
            i = -126, a == b is: true
            ........................
            ........................
            ........................
            i = 125, a == b is: true
            i = 126, a == b is: true
            i = 127, a == b is: true
            i = 128, a == b is: false
            i = 129, a == b is: false
            i = 130, a == b is: false
            */
        }
    }
}
```

