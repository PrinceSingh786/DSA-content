# 📚 Java Collections Framework – ArrayList

> **Language:** Java  
> **Prerequisite:** Arrays, Loops, Functions  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a Collection?

A **Collection** is a group of objects stored together.

### Examples

- 👨‍🎓 List of Students
- 📚 List of Books
- 🏙️ List of Cities
- 🎯 List of Scores

Instead of creating multiple variables,

```java
int a = 10;
int b = 20;
int c = 30;
```

we can store everything together using an **ArrayList**.

```java
ArrayList<Integer> list = new ArrayList<>();
```

---

# 📖 Java Collections Framework

```text
                 Iterable
                     │
              Collection
        ┌────────┼────────┐
        │        │        │
      List      Set     Queue
        │
  ┌─────┴──────────────┐
  │                    │
ArrayList         LinkedList
```

Today we study **ArrayList**.

---

# 📖 What is an ArrayList?

An **ArrayList** is a **Resizable (Dynamic) Array**.

Unlike normal arrays,

- ✅ Size can increase automatically.
- ✅ Size can decrease automatically.
- ✅ Easy insertion and deletion.
- ✅ Provides many built-in methods.

---

# 📖 Why do we need ArrayList?

## Normal Array

```java
int[] arr = new int[5];
```

### Problems

- Fixed size
- Cannot grow
- Cannot shrink
- Less flexible

---

## ArrayList

```java
ArrayList<Integer> list = new ArrayList<>();
```

### Advantages

- Dynamic size
- Easy to use
- Built-in methods
- Better for real-world applications

---

# 📖 Syntax

## Integer ArrayList

```java
ArrayList<Integer> list = new ArrayList<>();
```

---

## String ArrayList

```java
ArrayList<String> names = new ArrayList<>();
```

---

## Character ArrayList

```java
ArrayList<Character> letters = new ArrayList<>();
```

---

# 📖 Import Statement

```java
import java.util.ArrayList;
```

or

```java
import java.util.*;
```

---

# 📖 Creating an ArrayList

```java
ArrayList<Integer> list = new ArrayList<>();
```

Initially

```text
[]
```

---

# 📖 Printing an ArrayList

```java
System.out.println(list);
```

Output

```text
[]
```

---

# 📖 Built-in Functions

---

## ➜ add()

Adds element at the end.

```java
list.add(10);
list.add(20);
list.add(30);
```

Output

```text
[10, 20, 30]
```

---

## ➜ add(index, value)

Insert at a specific position.

```java
list.add(1, 100);
```

Before

```text
[10, 20, 30]
```

After

```text
[10, 100, 20, 30]
```

---

## ➜ get(index)

Returns element at given index.

```java
System.out.println(list.get(2));
```

Output

```text
20
```

---

## ➜ set(index, value)

Replace an element.

```java
list.set(1, 500);
```

Before

```text
[10, 100, 20]
```

After

```text
[10, 500, 20]
```

---

## ➜ remove(index)

Remove element by index.

```java
list.remove(2);
```

---

## ➜ remove(Object)

Remove first occurrence of a value.

```java
list.remove(Integer.valueOf(20));
```

---

## ➜ size()

Returns number of elements.

```java
list.size();
```

---

## ➜ contains()

Checks if element exists.

```java
list.contains(30);
```

Output

```text
true
```

---

## ➜ isEmpty()

```java
list.isEmpty();
```

---

## ➜ clear()

Removes all elements.

```java
list.clear();
```

Output

```text
[]
```

---

## ➜ indexOf()

Returns first occurrence.

```java
list.indexOf(30);
```

---

## ➜ lastIndexOf()

Returns last occurrence.

```java
list.lastIndexOf(30);
```

---

## ➜ Collections.sort()

Ascending order.

```java
Collections.sort(list);
```

---

## ➜ Collections.reverse()

```java
Collections.reverse(list);
```

---

## ➜ Collections.max()

```java
Collections.max(list);
```

---

## ➜ Collections.min()

```java
Collections.min(list);
```

---

## ➜ Collections.shuffle()

```java
Collections.shuffle(list);
```

---

## ➜ Collections.frequency()

```java
Collections.frequency(list, 10);
```

---

# 📖 Traversing an ArrayList

---

## Method 1 — Using for Loop ⭐

```java
for(int i = 0; i < list.size(); i++)
{
    System.out.println(list.get(i));
}
```

---

## Method 2 — Enhanced for Loop ⭐⭐

```java
for(int x : list)
{
    System.out.println(x);
}
```

---

## Method 3 — Iterator ⭐⭐⭐

```java
Iterator<Integer> it = list.iterator();

while(it.hasNext())
{
    System.out.println(it.next());
}
```

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| add() at end | O(1) Amortized |
| get() | O(1) |
| set() | O(1) |
| contains() | O(n) |
| remove(last) | O(1) |
| remove(first) | O(n) |
| insert(first) | O(n) |
| insert(last) | O(1) |

---

# 📖 Internal Working

Suppose the capacity is **4**

```text
Capacity = 4

┌───┬───┬───┬───┐
│10 │20 │30 │40 │
└───┴───┴───┴───┘
```

Now insert **50**

Java creates a larger array.

```text
Old Array

┌───┬───┬───┬───┐
│10 │20 │30 │40 │
└───┴───┴───┴───┘

        ↓ Resize

New Array

┌───┬───┬───┬───┬───┬───┬───┐
│10 │20 │30 │40 │50 │   │   │
└───┴───┴───┴───┴───┴───┴───┘
```

Capacity grows automatically (typically by **1.5×** in Java).

---

# 📖 Beginner Practice Problems ⭐

## Easy

1. Print all elements
2. Find sum
3. Find average
4. Find maximum
5. Find minimum
6. Count even numbers
7. Count odd numbers
8. Reverse printing
9. Search an element
10. Count frequency of an element

---

## Easy-Medium

11. Remove even numbers
12. Remove odd numbers
13. Replace negative numbers with zero
14. Find second largest element
15. Find second smallest element
16. Count positive numbers
17. Count negative numbers
18. Copy one ArrayList into another
19. Merge two ArrayLists
20. Swap two elements

---

## Medium

21. Remove duplicates
22. Rotate left by K positions
23. Rotate right by K positions
24. Check palindrome
25. Sort ascending
26. Sort descending
27. Find missing number
28. Move all zeros to end
29. Move all zeros to beginning
30. Remove all occurrences of a value

---

# 📖 LeetCode Problems

## 🟢 Easy

- 1929. Concatenation of Array
- 1480. Running Sum of 1D Array
- 1431. Kids With the Greatest Number of Candies
- 1365. How Many Numbers Are Smaller Than the Current Number
- 1295. Find Numbers with Even Number of Digits
- 905. Sort Array By Parity

---

## 🟡 Medium

- 1. Two Sum
- 26. Remove Duplicates from Sorted Array
- 27. Remove Element
- 88. Merge Sorted Array
- 189. Rotate Array
- 283. Move Zeroes
- 347. Top K Frequent Elements
- 49. Group Anagrams
- 56. Merge Intervals
- 57. Insert Interval

---

## 🔴 Hard (After HashMap & Advanced DSA)

- 4. Median of Two Sorted Arrays
- 239. Sliding Window Maximum
- 315. Count of Smaller Numbers After Self
- 327. Count of Range Sum
- 493. Reverse Pairs

---

# 📖 Common Interview Questions

1. Difference between Array and ArrayList?
2. Why can't we store `int` directly?
3. What is Autoboxing?
4. What is Unboxing?
5. Why is `get()` O(1)?
6. Why is insertion at the beginning O(n)?
7. Why is deletion from the middle O(n)?
8. Difference between `remove(index)` and `remove(Object)`?
9. Difference between `size()` and `length`?
10. Difference between ArrayList and LinkedList?

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction to Collections
- Array vs ArrayList
- Creating an ArrayList
- add()
- get()
- set()
- remove()
- size()
- Printing
- Traversal
- 10 Beginner Problems

---

## 🟡 Lecture 2

- contains()
- clear()
- indexOf()
- lastIndexOf()
- sort()
- reverse()
- max()
- min()
- shuffle()
- frequency()
- 10 Intermediate Problems

---

## 🔴 Lecture 3

- Internal Working
- Capacity & Resizing
- Time Complexity
- Iterator
- Interview Questions
- LeetCode Practice
- Introduction to LinkedList