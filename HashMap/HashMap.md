# HashMap

## **put**:修改value

> **put(K key, V value)**\
@Param: key 键 value 值\
@Return: 如果key已经存在，则会将值更新为value。返回值为更改前的value，如果key不存在则返回null。
```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<Integer, Integer> map = new HashMap<>();
        System.out.println( map.put(1, 1));
        System.out.println(map.put(1,2));
    }
}

```

## putAll:将指定的Map中所有键值对添加

```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<Integer, Integer> map = new HashMap<>();
        System.out.println( map.put(1, 1)); // return null
        System.out.println(map.put(1,2)); // return 1
        HashMap<Integer, Integer> map2 = new HashMap<>();
        map2.putAll(map);
        for (Integer x : map.keySet()) {
            System.out.println(map.get(x));// out 2
        }
    }
}
```

## get:获取指定key所对应的value，如果不存在则返回null。

## getOrDefault:返回指定key对应的值，如果key不存在则返回指定的默认值。
```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < 10; i++) {
            map.put(i, i);
        }
        // map 有 0-9对应的值
        System.out.println(map.getOrDefault(1, 0)); // out 1
        System.out.println(map.getOrDefault(10, -1)); // out -1
    }
}
```

## entrySet()

返回一个包含值对的Set集和，可以使用迭代器来遍历所有的键值对。

## remove

从`HashMap`中移除指定key对应的键值对，并返回被删除key对应的value，如果键不存在，则返回`null`。
```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < 10; i++) {
            map.put(i, 9 - i);
        }
        // map 有 0-9对应的key,分别对应9-0
        System.out.println(map.remove(1)); // out 8
        System.out.println(map.remove(10)); // out null
        System.out.println(map.get(1)); // out null
    }
}
```

## clear()

清空`HashMap`的所有键值对，使其变为空

```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < 10; i++) {
            map.put(i, 9 - i);
        }
        // map 有 0-9对应的key,分别对应9-0
        map.clear();
        System.out.println(map.size());
    }
}

```

## keySet()

返回一个包含所有键的`Set`集合。

## values()

返回一个包含所有`value`的集合。

## containsKey() | containsValue()

判断`HashMap`中是否包含指定的`value` or `key`。

```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < 10; i++) {
            map.put(i, 19 - i);
        }
        // map 有 0-9对应的key,分别对应19-10
        System.out.println(map.containsValue(1));
        System.out.println(map.containsValue(19));
        System.out.println(map.containsKey(1));
        System.out.println(map.containsKey(19));
    }
}

```

