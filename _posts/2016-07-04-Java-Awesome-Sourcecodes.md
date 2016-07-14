---
layout: post
title: Java精巧源代码收集
date: 2016-07-04 16:06:31
permalink: java-awesome-sourcecodes
disqus: y
---




```java
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
# HashMap类中的一个方法, 求大于或等于指定数字的最小2的幂

```java
private static int binarySearch0(long[] a, int fromIndex, int toIndex,
                                     long key) {
        int low = fromIndex;
        int high = toIndex - 1;

        while (low <= high) {
            int mid = (low + high) >>> 1;
            long midVal = a[mid];

            if (midVal < key)
                low = mid + 1;
            else if (midVal > key)
                high = mid - 1;
            else
                return mid; // key found
        }
        return -(low + 1);  // key not found.
    }
```
# 这是Arrays类中的一个二分查找法，二分查找法本身没有什么特别之处，关键是返值-(low + 1)，即如果没有查找到，返回的并非-1,而是跟low的位置有关系，low表示的是大于key的最小index。
