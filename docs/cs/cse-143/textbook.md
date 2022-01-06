---
layout: default
title: Textbook Notes
parent: CSE 143
grand_parent: Computer Science
nav_order: 2
---

# Textbook Notes

CSE 143
{: .fs-6 .fw-300 }

---

## Navigation

---

## Chapter 10: ArrayLists

### 10.1: ArrayLists
- Lists should be dynamic, flexible. We want to list to grow and shrink over time as we add or remove values.
- We are considering a list abstraction.
- Java provides the `ArrayList` that provides the same fast random access as an array while letting you make simple requests to add or remove values.
- `ArrayList<E>` is the generic class in Java. `E` is short for Element.


- The `Arraylist` is part of the `java.util` package; import it before the program.
- `ArrayList<String> list = new ArrayList<String>();`
- `.size()` can be used to access the number of elements in the `ArrayList`.

Basic `ArrayList` Methods:

| Method | Description |
| --- | --- |
| `add(value)` | Adds a value to the end of the list. |
| `add(index, value)` | Adds a value to the specified index. |
| `clear` | Removes all elements from list. |
| `get(index)` | Gets item at specified index. |
| `remove(index)` | Removes a value at the specified index. |
| `set(index, value)` | Replaces the value at the given index with the current value. |
| `size()` | Returns the current number of elements in the list. |

`ArrayList` Searching Methods:

| Method | Description |
| --- | --- |
| `contains(value)` | `true` if item value appears in list, `false` otherwise. |
| `indexOf(value)` | Returns the index of the 1st occurrence of the given value, and `-1` if not found. |
| `lastIndexOf(value)` | Returns the index of the last occurrence of the given value, and `-1` if not found. |

You can use a `for-each` loop to iterate over elements of an `ArrayList` directly instead of using for-loop indexing.

```java
for (<type> <name> : <structure>) {
  <statement>
}
```

This is equivalent to the Python

```python
for name in structure:
  statement
```

However, you cannot modify an ArrayList while you are iterating through it using the `for-each` method.

Because `ArrayList<E>` can only store objects, it cannot store primitive types (`int`, `double`, `char`, `boolean`, etc.). Java defines wrapper classes that 'wrap' around primitive data.

```java
int x = 38;
Integer y = new Integer(38);
int number = y.intValue();

ArrayList<Integer> list = new ArrayList<Integer>();
list.add(13);
list.add(47);
```

Boxing: automatic conversion from primitive data to a wrapped object of the appropriate type, like `int` boxed to form `Integer`.

Common Wrapper Classes:

| Primitive Type | Wrapper Class |
| --- | --- |
| `int` | `Integer` |
| `double` | `Double` | 
| `char` | `Character` |
| `boolean` | `Boolean` |

---

## Chapter 11: Java Collections Framework

### 11.2: Sets
- Limitation to linked and array lists: searching takes a long time.
- *Set* abstract data type: a collection that cannot contain duplicates, and thus is faster to search.
  - Sets also easily eliminate duplicates.
- Two primarily implementations: `HashSet` and `TreeSet`. The former is the general-purpose set class.

```java
Set<String> names = new HashSet<String>();
names.add("Adam");
names.add("Eve");
names.add("Steve");
names.add("Adam"); // will not be added
```

- The `Set` interface provides all operations from the `Collection` interface, like `add`, `contains`, and `remove`.
- `contains` in `ArrayList` and `LinkedList` examines every element in the collection until it finds the target value.
- `HashSet`s use a hash table, which places elements in specific positions based on integers called hash codes; this allowed for fast addition, rmeoval, and search.
  - However, the hashing technique forces elements to be arranged in an unpredictable order.
  - `LinkedHashSet` is almost as fast as `HashSet`, but stores elements in the order they were inserted.
- `HashSet` can also accept another collection and puts unique elements into a `Set`. This can be used to find if a `List` has any duplicates by comparing sizes of the original list and the set of unique values:

```java
public static boolean hasDuplicates(List<Integer> list) {
  Set<Integer> set = new HashSet<Integer>(list);
  return set.size() < list.size();
}
```
- `HashSet` does not support indexing; to iterate, use one of the following two methods:
  - *Iteration*. `Iterator<String> itr = set.iterator(); while (itr.hasNext()) {...}`
  - *For-each*. `for (String item: set) {...}`
- `TreeSet` uses an internal linked data structure called a binary search tree to store elements in sorted order.
  - Efficient for adding, removing, and searching, albeit slower than `HashSet`.
  - `TreeSet` can be applied to data with a *natural ordering* specified by a `Comparable` interface, like `Integer` or `String`.
  - Do not use `TreeSet` with objects without a natural ordering/unspecified comparator.

*Common set operations given sets `A` and `B`*:

| Set Operation | Method | Description |
| --- | --- | --- |
| union | `addAll` | Set of all elements in A, B, or both |
| intersection | `retainAll` | Set of all elements that are in both A and B |
| difference | `removeAll` | Set of all elements in A but not in B |
| superset/subset | `containsAll` | Returns if A is a superset of B |

- Set operations modify existing sets rather than creating new ones.

---

## Chapter 15: Implementing a Collection Class

### 15.1: Single ArrayIntList
- Clients don't want to understand all the internal class details.
- Contract - specification telling the client how an object behaves without describing the implementation details.
- `ArrayIntList` - we use an unfilled array in which some of the elements are filled.
- Distinguish between occupied and vacant cells with a `size` variable.


We can write a `print`/`toString` method that displays the internal contents of the list:

```java
public void toString() {
  if (size == 0) {
    System.out.println("[]");
  } else {
    System.out.print("[" + elementData[0]);
    for (int i = 1; i < size; i++) {
      System.out.print(", " + elementData[i]);
    }
    System.out.println("]");
  }
}
```
To allow the user to access the size, we can write an accessor method:
```java
public int size() {
  return size;
}
```
To remove an item at a given index, we shift all values after the index down by one position.
```java
public void remove(int index) {
  for (int i = index; i < size – 1; i++) {
    elementData[i] = elementData[i + 1];
  }
  size– –;
}
```
To insert an item at a given index, we go in the other direction and shift all values after the index up by one position.
```java
public void add(int index, int value) {
  for (int i = size; i >= index + 1; i– –) {
    elementData[i] = elementData[i – 1];
  }
  elementData[index] = value;
  size++;
}
```
To set a default capacity size in addition to offering parameter inputs, we define two separate methods. These have different *signatures* (one takes arguments, one does not).
```java
public ArrayIntList() {
  this(100);
}

public ArrayIntList(int capacity) {
  elementData = new int[capacity];
  size = 0;
}
```

### 15.2: A More Complete ArrayIntList

We can make preconditions explicit by throwing errors with optional error messages:
```java
if (capacity < 0) {
  throw new IllegalArgumentException("capacity: " + capacity);
}
```

Common exception types:

| Exception Type | Description |
| --- | --- |
| `NullPointerException` | A `null` value has been used in a case that requires an object. |
| `ArrayIndexOutOfBoundsException` | A passed index is illegal. |
| `IndexOutOfBoundsException` | A passed index to a nonarray object is illegal. |
| `IllegalStateException` | A method has been called in an illegal time. |
| `IllegalArgumentException` | A value passed to a method is illegal. |
| `NoSuchElementException` | A call was made to a `next` method when no such value exists. |

Common convenience methods:

| Method Name | Description |
| `indexOf` | Searches for the index of a value in the array. |
| `contains` | Returns a Boolean indicating the presence of a value in the array. |
| `isEmpty` | Returns whether the array is empty or not; i.e. `return size==0`. |
| `set` | Directly sets an index to a new value, rather than using `remove`, then `add`. |
| `addAll` | Adds all elements from anohter `ArrayIntList`.


---
