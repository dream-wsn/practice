# Map集合

```java
1.Map集合是一个双列集合，一个元素包含两个值（一个key，一个value）
2.Map集合中的元素，key和value的数据类型可以相同，也可以不同
3.Map集合中的元素，key是不允许重复的，value是可以重复的
4.Map集合中的元素，key和value是一一对应
```

**HashMap<k,v>集合 implements Map<k，v>接口**

```
HashMap集合的特点：
   1.HashMap集合底层是哈希表：查询的速度特别的快
       JDK1.8之前：数组+单向链表
       JDK1.8之后：数组+单向链表/红黑树（链表的长度超过8）：提高查询的速度
   2.hashMaoihe是一个无序的集合，存储元素和取出元素的顺序有可能不一致
```

**LinkedHashMap<k,v>集合 extends HashMap<k,v>集合**

```
LinkedHashMap的特点：
   1.LinkedHashMap集合底层是哈希表+链表（保证迭代的顺序）
   1.LinkedHashMap集合是一个有序的集合，存储元素和取出元素的顺序是一致的
```

Map常用方法：

put(K key, V value) 
          将指定的值与此映射中的指定键关联（可选操作）。 

get(Object key) 
          返回指定键所映射的值；如果此映射不包含该键的映射关系，则返回 null。

containsKey(Object key) 
          如果此映射包含指定键的映射关系，则返回 true。

keySet() 
          返回此映射中包含的键的 Set 视图。

entrySet() 
          返回此映射中包含的映射关系的 Set 视图。把Map集合内部的多个Entry对象取出来存储到一个Set集合中





Map.Entry<K,V>:在Map接口中有一个内部接口Entry

作用：当Map接口以创建，那么就会在Map集合中创建一个Entry对象，用来记录键与值（键值对对象，键与值的映射关系）-->**结婚证**

**Map.Entry()方法**

getKey() 
          返回与此项对应的键。

getValue() 
          返回与此项对应的值。

setValue(V value) 
          用指定的值替换与此项对应的值（可选操作）。

**HashMap存储自定义类型键值**

Map集合保证key是唯一的： 作为key1的元素，必须重写hashCode 和 equals方法，以保证key的唯一

HashCode存储自定义类型键值
key：String类型
			String类重写hashCode方法和equals方法，可以保证key唯一
value：Person类型
			value可以重复（同名同年龄视为同一个）



### Hashtable<K,V>

Hashtable<K,V>集合 implements Mop<K,V>接口

Hashtable：底层也是一个哈希表，是一个线程安全的集合，是单线程集合，速度慢
HashMap：底层也是一个哈希表，是一个现场不安全的集合，是多线程的集合，速度快
HashMap集合（之前学的所有的集合）：可以存储null值，null键
Hashtable集合，不能存储null值，null键

Hashtable和Vector集合一样，在jdk1.2版本之后被更先进的集合（hashMap，ArrayList）取代了
Hashtable的子类Properties依然活跃在历史舞台
*Properties集合是一个唯一和IO流结合的集合*







同步的



