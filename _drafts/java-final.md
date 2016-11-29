**Java final关键字的用法**

final修饰过的变量，它在编译时被解析为常量值的一个本地拷贝，存储到自己的常量池，或嵌入到它的字节码流中。

```Java
String s0 = "aabb";
String s1 = "aa";
System.out.println(s0 == s1 + "bb"); // false;
```
使用final修饰后

```Java
String s0 = "aabb";
final String s1 = "aa";
System.out.println(s0 == s1 + "bb"); // true;
```


final只对引用的“值”（即内存地址）有效，它迫使引用只能指向初使指向的那个对象，再次改变它的指向会导致编译期错误，即便新指向的地址，是final修饰对象本身的地址也不行；

```Java
final String s1 = "aa";
s1 = "bb"; // 此句无法通过编译
```

至于该引用指向对象的变化，final是不负责的。

```Java
final StringBuilder s = new StringBuilder("aa");
s.append("bb"); // 编译通过
```