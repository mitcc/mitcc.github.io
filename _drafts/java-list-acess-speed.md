```java
public class Test {

    static ArrayList<Integer> arrayList = new ArrayList<Integer>();
    static LinkedList<Integer> linkedList = new LinkedList<Integer>();

    static final int N = 100000;  // N = 1000000, 10000000, 100000000...

    public static void main(String[] args) {
        long start = System.nanoTime();
        for (int i = 0; i < N; ++i) {
            arrayList.add(i);
        }
        long end = System.nanoTime();
        System.out.println("ArrayList's ADD time is " + (end - start) / 1000 + " ms.");

        start = System.nanoTime();
        for (int i = 0; i < N; ++i) {
            linkedList.add(i);
        }
        end = System.nanoTime();
        System.out.println("LinkedList's ADD time is " + (end - start) / 1000 + " ms.");
    }

}
```

使用add方法将元素添加至List末尾，

当N=100000时，ArrayList用时比LinkedList久；

当N=1000000时，ArrayList用时少于LinkedList

**上面N的取值并非准确的临界值，只是随便取的一个实验值**
