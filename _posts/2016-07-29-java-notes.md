---
title: Java学习笔记
date: 2016-07-29 00:53:47
---



Java Arrays类源代码中的fill方法，使得**数组中的每个元素，填充同一个对象的引用，而非将val复制a.length个，分别指向这些对象**，下面是fill方法的源代码。

```java
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
        // method 1
        public static int abs(int a) {
            return (a < 0) ? -a : a;
        }

        // method 2
        public static long abs(long a) {
            return (a < 0) ? -a : a;
        }

        // method 3
        public static float abs(float a) {
            return (a <= 0.0F) ? 0.0F - a : a;
        }

        // method 4
        public static double abs(double a) {
            return (a <= 0.0D) ? 0.0D - a : a;
        }
```

当a为Integer.MIN_VALUE,也即-2147483648时，Math.abs(a)使用的是方法1，返回结果为原值：-2147483648。
