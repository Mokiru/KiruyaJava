# Java Object 类

Java Object 类是所有类的父类，也就是说Java的所有类都继承了Object，**子类可以使用Object的所有方法**。

Object类位于java.lang包中，编译时会自动导入，我们创建一个类时，如果没有明确继承一个父类，那么它就会自动继承Object，成为Object的子类。

Object可以显式继承，也可以隐式继承，一下两种方法是一样的：

显式继承：

```java
public class Kiruya extends Object {

}
```

隐式继承：
```java
public class Kiruya {

}
```

# 类的方法

`protected Object clone()`：创建并返回一个对象的拷贝。

`boolean equals(Object obj)`：比较两个对象是否相等。

`protected void finalize()`：当GC（垃圾回收器）确定不存在对该对象的有更多引用时，由对象的垃圾回收器调用此方法。

`Class<?> getClass()`：获取对象的运行时对象的类。

`int hashCode()`：获取对象的hash值。

`void notify()`：唤醒在该对象上等待的所有线程。

`String toString()`：返回对象的字符串表示形式。

`void wait()`：让当前线程进入等待状态。直到其他线程调用此对象的`notify()`方法或`notifyAll()`方法。

`void wait(long timeout)`：让当前线程处于等待（阻塞）状态，直到其他线程调用此对象的`notify()`方法或`notifyAll()`方法，或者超过参数设置的timeout超时时间。

`void wait(long timeout, int nanos)`：与上一个方法类似，多了一个`nanos`参数，这个参数表示额外时间（以纳秒为单位，范围是0-999999）。所以超时的时间还需要加上nanos纳秒。