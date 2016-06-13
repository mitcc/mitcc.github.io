---
layout: post
title: Java装箱与拆箱
date: 2015-04-01 14:21:25
permalink: Java-Boxing-and-Unboxing
disqus: y
---

# 集合中只能存放对象1

==  集合中只能存放对象2

## 集合中只能存放对象3

### 集合中只能存放对象4

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

##### TEXT
这是文字，文字文字文字

def hi():
    return "Hi, mitcc!!!"

上面是Python
