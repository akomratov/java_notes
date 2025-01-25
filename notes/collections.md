# Collections
Collections don't accept **primitive** types.

Use **wrapper** classes.

* **List**
  - ArrayList
  - LinkedList
  - Vector
  - Stack
* **Set**
  - HashSet
  - TreeSet
  - LinkedHashSet
* **Queue**
  - PriorityQueue
  - ArrayDeque
* **Map**
  - HashMap
  - TreeMap
  - HashTable


## Generics
Controlling inner objects types with implicit **casting**.


Generics examples:
```java
// one inner type
ArrayList<Integer> list = new ArrayList<Integer>();

// two inner types
HashMap<Integer, String> map = new HashMap<Integer, String>();

// Generic as an inner type
ArrayList<ArrayList<String>> lists = new ArrayList<ArrayList<String>>();

public class MultiPart<T, E> extends AbstractPart<E> {
   // ...
}

public class Part<T extends SuperT> {
   // ...
}


```


## ArrayList

Syntax sugar:
```java
ArrayList<String> list = new ArrayList<String>();
list.add("Hello");
list.add("world");

ArrayList<String> list1 = new ArrayList<String>()
{{
   add("Hello");
   add("world");
}};

var list2 = new ArrayList<String>()
{{
   add("Hello");
   add("world");
}};
```

