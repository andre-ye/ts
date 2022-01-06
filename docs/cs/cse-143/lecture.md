---
layout: default
title: Lecture Notes
parent: CSE 143
grand_parent: Computer Science
nav_order: 1
---

# Lecture Notes

CSE 143
{: .fs-6 .fw-300 }

---

## Navigation

---

## Week 1 Monday - ArrayIntList Add, Remove, toString Methods
- CSE 143 centers around data structures (linked lists, binary trees, Collections classes), as well as recursion for control.
- Riel's perspective of an objective: external vs internal views.
  - External: client side, *what* an object does
  - Internal: implementation, *how* an object works
- Running data structure: `ArrayList<E>`. `ArrayList` that can store different types of elements.
- Ideally, you should work in a programming environment. Recommended environment is JGrasp.

`ArrayList` review:

```java
ArrayList<String> list = new ArrayList<>();
list.add("four");
list.add("score");
list.add("seven");
list.add("years");
list.add("ago");
list.add(2, "and");
```
Appends items to the end at default. If an index is provided, inserts at that index.

*How is this done?* The `ArrayList` can be thought of as growing and shrinking, but it's not actually growing and shrinking inside.

Two numbers to think about: capacity and size.
- A variable size is used to keep track of how many 'things' are currently inside the structure.
- Arrays have a certain associated capacity

**Let's think about implementing the internal representation for `ArrayIntList`.**

Initializing the class fields:
```java
public class ArrayIntList {
  int[] elementData;
  int size;
}
```

> Style Issue Notice (!)

Never initialize values outside of a constructor function.
```java
public class ArrayIntList {
  int[] elementData = new ...;
  int size = ...;
}
```
Instead, use a constructor function:
```java
  public ArrayIntList() {
    elementData = new int[100];
    size = 0;
  }
```

The `ArrayIntList` object should include a method to add new elememnts. We rely upon the internal state of `size` to determine which slot in `elementData` to use.
```java
  public void add(int value) {
    this.elementData[size] = value;
    this.size++;
  }
```

You want to have a `toString()` method in your function to display the desired representaiton when `System.out.print` is called.

Next lecture -- it will be important to use the keyword `private` for fields.

---

## Week 1 Wednesday - ArrayIntList Methods

CSE Grades by Lectures Watched from Spring 2021:

| Lectures Watched | # Students | Avg Grade |
| --- | --- | --- |
| 90-100% | 121 | 3.32 |
| 80-90% | 113 | 3.06 |
| 70-80% | 31 | 2.88 |
| 60-70% | 24 | 2.86 |
| 0-60% | 126 | 1.97 |

In this class, many resources are presented (lecture, section, textbook). You do not need to utilize all of them.


`toString()` methods allow us to print a representation of the method. When calling `System.out.println(obj)`, the `toString` method of `obj` is implicitly called. The same occurs with String arithmetic: `"hello " + obj`.

**Use this class' `ArrayIntList` as an example for Homework 1.**

> OOPSLA: An object encapsulates state and exposes behavior.

- *State*: represents by fields, the data an object keeps track of.
- *Behavior*: represented by methods.
- *Encapsulation*: the client cannot 'reach right in'; the internal functionalities and operations are kept protected/encapsulated. We can utilize the `private` keyword for object fields to achieve encapsulation.

*Make sure to look at style issues for a particular homework.*

While the client should not be able to *modify* certain fields, we can create *getter methods* that return the value of a field.

Contract with the client: `pre/post` format.
```java
// contract
// pre : index >= 0 and index < size
// post: returns the value at a given index

public int get(int index) {
  if (index < 0 || index < size) {
    throw new ExceptionType(message);
  }
  return elementData[index];
```

Overloading: two different constructors.

Adhere to Boolean Zen: directly return the result of a conditional if a Boolean output is desired.

`private` means accessible to the class, including all instances of that class.

---
