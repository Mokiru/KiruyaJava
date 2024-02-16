# ArrayList

ArrayList 类是一个可以动态修改的**数组**，与普通数组的区别就是它是没有固定大小的限制，我们可以添加或删除元素。

ArrayList继承了AbstractList，并且实现了List接口。

![image](../图片/ArrayList/ArrayList-1.png)

ArrayList 类位于java.util包中，使用前需要引入它，语法格式如下：
```java
import java.util.ArrayList; // 引入 ArrayList 类

ArrayList<E> objectName = new ArrayList<>(); // 初始化
```

- E:泛型数据类型，用于设置objectName的数据类型，只能为引用数据类型。
- objectName:对象名

ArrayList 是一个数组队列，提供了相关的添加、删除、修改、遍历等功能

## 添加元素

ArrayList 类提供了很多有用的方法，添加元素到ArrayList 可以使用`add()`方法：
```java
import java.util.ArrayList;

public class Kiruya {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<String>();
        list.add("Kokoro");
        list.add("Momochi");
        System.out.println(list);
    } 
}
```

以上实例，执行的输出结果为：

> [Kokoro, Momochi]

## 访问元素

访问ArrayList 中的元素可以使用`get()`方法：

```java
import java.util.ArrayList;

public class Kiruya{
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<String>();
        list.add("Kokoro");
        list.add("Momochi");
        System.out.println(list.get(0));
    }
}
```
以上实例，执行输出结果为：

> Momochi

## 修改元素

如果要修改ArrayList 中的元素可以使用`set()`方法：
```java
import java.util.ArrayList;

public class Kiruya{
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<String>();
        list.add("Kokoro");
        list.add("Momochi");
        list.set(0, "Kiruya"); // 修改 index = 0 的位置 的元素 为Kiruya
        System.out.println(list);
    }
}
```

以上实例，执行输出结果为：

> [Kiruya, Momochi]

## 删除元素

如果要删除ArrayList 中的元素可以使用`remove()`方法：
```java
import java.util.ArrayList;

public class Kiruya {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<String>();
        list.add("Kokoro");
        list.add("Momochi");
        list.remove(1);
        System.out.println(list);
    }
}
```

以上实例，执行输出结果为：

> [Kokoro]

## 计算大小

如果要计算ArrayList中的元素数量可以使用`size()`方法：
```java
import java.util.ArrayList;

public class Kiruya {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Kokoro");
        list.add("Momochi");
        System.out.println(list.size());
    }
}
```
以上实例，执行输出结果为：

> 2

## 迭代数组列表

我们可以使用`for`来迭代数组列表中的元素：
```java
import java.util.ArrayList;

public class Kiruya {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Kokoro");
        list.add("Momochi");
        for (int i = 0; i < list.size(); i++) {
            System.out.println(list.get(i));
        }
    }
}
```

以上实例，执行输出结果为：

> Kokoro
> Momochi

也可以使用`for-each`来迭代元素：

```java
import java.util.ArrayList;

public class Kiruya {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Kokor");
        list.add("Momochi");
        for (String i : list) {
            System.out.println(i);
        }
    }
}
```

## 排序

Collections 类也是一个非常有用的类，位于java.util包中，提供的`sort()`方法可以对字符或数字列表进行排序。

以下实例对字母进行排序：

```java
import java.util.ArrayList;
import java.util.Collections;

public class Kiruya {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Kokoro");
        list.add("Momochi");
        Collections.sort(list); // 默认从小到大排序
        for (String i : list) {
            System.out.println(i);
        }
    }
}
```

以上实例，执行输出结果为：

> Kokoro
> Momochi

## 其余方法

`subList(int fromIndex, int toIndex)`：截取arraylist中$[fromIndex, toIndex)$部分。

`toArray()`：将arraylist转换为数组。

`toString()`：将arraylist转换为字符串。


