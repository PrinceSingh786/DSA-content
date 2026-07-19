# 🟢 Java Collections Framework – HashSet

> **Language:** Java  
> **Prerequisite:** Arrays, ArrayList, HashMap  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a HashSet?

A **HashSet** is a collection that stores **unique elements**.

It automatically removes duplicate values.

Unlike ArrayList,

- ❌ No duplicate elements
- ❌ No indexing
- ❌ No guaranteed insertion order
- ✅ Fast searching
- ✅ Fast insertion

---

# 📖 Real-Life Examples

## 🎓 Unique Roll Numbers

```text
101
102
103
104
```

Duplicate roll numbers are not allowed.

---

## 🌎 Unique Country Names

```text
India
USA
Japan
China
```

---

## 📧 Registered Email IDs

Every email must be unique.

```text
abc@gmail.com
xyz@gmail.com
pqr@gmail.com
```

---

# 📖 Why do we need HashSet?

Suppose we store

```text
10 20 10 30 20 40
```

Using ArrayList

```java
[10,20,10,30,20,40]
```

Duplicates remain.

Using HashSet

```java
[10,20,30,40]
```

Duplicates are automatically removed.

---

# 📖 Properties of HashSet

- Stores only unique elements
- Duplicate elements are ignored
- No indexing
- Fast searching
- Does not maintain insertion order
- Allows one `null` value

---

# 📖 Import Statement

```java
import java.util.HashSet;
```

or

```java
import java.util.*;
```

---

# 📖 Creating a HashSet

## Integer

```java
HashSet<Integer> set = new HashSet<>();
```

---

## String

```java
HashSet<String> set = new HashSet<>();
```

---

## Character

```java
HashSet<Character> set = new HashSet<>();
```

---

# 📖 Printing HashSet

```java
System.out.println(set);
```

Initially

```text
[]
```

---

# 📖 Built-in Functions

---

## ➜ add()

Adds an element.

```java
set.add(10);
set.add(20);
set.add(30);
```

Output

```text
[10,20,30]
```

---

## Duplicate Element

```java
set.add(20);
```

Output

```text
[10,20,30]
```

Nothing happens.

---

## ➜ remove()

```java
set.remove(20);
```

Output

```text
[10,30]
```

---

## ➜ contains()

```java
set.contains(30);
```

Output

```text
true
```

---

## ➜ size()

```java
set.size();
```

---

## ➜ clear()

```java
set.clear();
```

---

## ➜ isEmpty()

```java
set.isEmpty();
```

---

# 📖 Traversing HashSet

---

## Method 1 – Enhanced For Loop ⭐

```java
for(int x : set)
{
    System.out.println(x);
}
```

---

## Method 2 – Iterator ⭐⭐⭐

```java
Iterator<Integer> it = set.iterator();

while(it.hasNext())
{
    System.out.println(it.next());
}
```

---

# 📖 Internal Working

Suppose we insert

```java
set.add(25);
```

Internally

```text
25

↓

Hash Function

↓

Hash Code

↓

Bucket

↓

Store Element
```

Searching

```java
set.contains(25);
```

Again calculates the bucket and checks whether the element exists.

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| add() | O(1) Average |
| remove() | O(1) Average |
| contains() | O(1) Average |
| Traversal | O(n) |
| size() | O(1) |
| clear() | O(n) |

> Worst case for `add()`, `remove()`, and `contains()` is O(n), but average performance is O(1).

---

# 📖 Common Data Types

## Integer

```java
HashSet<Integer> set = new HashSet<>();
```

---

## String

```java
HashSet<String> set = new HashSet<>();
```

---

## Character

```java
HashSet<Character> set = new HashSet<>();
```

---

# 📖 Remove Duplicates from an Array

Input

```text
10 20 30 20 40 10 50
```

```java
HashSet<Integer> set = new HashSet<>();

for(int x : arr)
{
    set.add(x);
}

System.out.println(set);
```

Output

```text
[10,20,30,40,50]
```

---

# 📖 Union of Two Arrays

```java
HashSet<Integer> set = new HashSet<>();

for(int x : arr1)
    set.add(x);

for(int x : arr2)
    set.add(x);

System.out.println(set);
```

---

# 📖 Intersection of Two Arrays

```java
HashSet<Integer> set = new HashSet<>();

for(int x : arr1)
    set.add(x);

for(int x : arr2)
{
    if(set.contains(x))
        System.out.print(x + " ");
}
```

---

# 📖 Beginner Practice Problems ⭐

## Easy

1. Print all elements
2. Remove duplicates from an array
3. Count distinct elements
4. Search an element
5. Remove an element
6. Store unique strings
7. Store unique characters
8. Print size
9. Check if empty
10. Clear the set

---

## Easy-Medium

11. Union of two arrays
12. Intersection of two arrays
13. Find common elements
14. Check if two arrays have common elements
15. Find unique words in a sentence
16. Count distinct characters
17. Remove duplicate words
18. Check subset
19. Check superset
20. Find missing numbers using HashSet

---

## Medium

21. Longest Consecutive Sequence
22. Happy Number
23. Contains Duplicate
24. Contains Duplicate II
25. Find Difference of Two Arrays
26. Unique Morse Code Words
27. Valid Sudoku
28. Distinct Islands (Concept)
29. Word Break (Concept)
30. Set Matrix Zeroes (with HashSet)

---

# 📖 LeetCode Problems

## 🟢 Easy

- 217. Contains Duplicate
- 349. Intersection of Two Arrays
- 804. Unique Morse Code Words
- 705. Design HashSet
- 268. Missing Number
- 771. Jewels and Stones

---

## 🟡 Medium

- 128. Longest Consecutive Sequence
- 36. Valid Sudoku
- 2215. Find the Difference of Two Arrays
- 1429. First Unique Number
- 694. Number of Distinct Islands

---

## 🔴 Hard

- 30. Substring with Concatenation of All Words
- 212. Word Search II
- 381. Insert Delete GetRandom O(1) – Duplicates Allowed

---

# 📖 Common Interview Questions

1. Difference between HashSet and ArrayList?
2. Difference between HashSet and HashMap?
3. Can HashSet store duplicate elements?
4. Can HashSet store `null`?
5. Why is searching O(1)?
6. Why is there no indexing?
7. Why is insertion order not maintained?
8. How does HashSet remove duplicates?
9. What is a Hash Function?
10. What is a Bucket?

---

# 📖 HashSet vs ArrayList

| Feature | ArrayList | HashSet |
|----------|-----------|----------|
| Duplicate Elements | ✅ Allowed | ❌ Not Allowed |
| Indexing | ✅ Yes | ❌ No |
| Searching | O(n) | O(1) Average |
| Insertion Order | ✅ Maintained | ❌ Not Guaranteed |
| Random Access | ✅ Yes | ❌ No |

---

# 📖 HashSet vs HashMap

| HashSet | HashMap |
|----------|----------|
| Stores only values | Stores key-value pairs |
| No duplicate values | No duplicate keys |
| Uses `add()` | Uses `put()` |
| Uses `contains()` | Uses `containsKey()` |
| Internally backed by a HashMap | Stores keys and values |

---

# 📖 Real-World Applications

- Remove duplicate values
- Count distinct elements
- Spell Checker
- Unique User IDs
- Student Roll Numbers
- Email Registration
- Union & Intersection of Arrays
- Fast Lookup
- Duplicate Detection

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction
- Why HashSet?
- HashSet vs ArrayList
- Creating HashSet
- add()
- remove()
- contains()
- size()
- Traversal
- Beginner Problems

---

## 🟡 Lecture 2

- Remove Duplicates
- Count Distinct Elements
- Union
- Intersection
- Internal Working
- Time Complexity
- Intermediate Problems

---

## 🔴 Lecture 3

- HashSet vs HashMap
- HashSet vs TreeSet (Introduction)
- Interview Questions
- LeetCode Problems
- Real-world Applications