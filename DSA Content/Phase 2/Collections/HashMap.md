# 🗺️ Java Collections Framework – HashMap

> **Language:** Java  
> **Prerequisite:** Arrays, Loops, Functions, ArrayList  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a HashMap?

A **HashMap** is a data structure that stores data in **Key–Value pairs**.

Think of it like a dictionary.

```text
Key       Value
-------------
101  →    Prince
102  →    Rahul
103  →    Aman
```

Every **key** is unique.

Multiple keys **cannot** be the same.

Values **can** be duplicate.

---

# 📖 Real Life Examples

## 📱 Contacts

```text
Phone Number → Person Name

9876543210 → Prince
9123456789 → Rahul
```

---

## 🎓 Student Database

```text
Roll Number → Student Name

101 → Prince
102 → Aman
103 → Rahul
```

---

## 🌍 Country Capitals

```text
India → New Delhi
Japan → Tokyo
USA → Washington
```

---

# 📖 Why do we need HashMap?

Suppose we want to store

```text
101 → Prince
102 → Rahul
103 → Aman
```

Using ArrayList

```java
ArrayList<String> list = new ArrayList<>();
```

Searching by roll number becomes difficult.

Instead

```java
HashMap<Integer,String> map = new HashMap<>();
```

Now searching becomes much faster.

---

# 📖 HashMap Structure

```text
Key        Value

101  →  Prince
102  →  Rahul
103  →  Aman
104  →  Akash
```

---

# 📖 Important Properties

- Stores Key-Value pairs
- Keys are unique
- Values can be duplicate
- No indexing
- Fast Searching
- Does not maintain insertion order

---

# 📖 Import Statement

```java
import java.util.HashMap;
```

or

```java
import java.util.*;
```

---

# 📖 Creating a HashMap

```java
HashMap<Integer,String> map = new HashMap<>();
```

---

# 📖 Printing HashMap

```java
System.out.println(map);
```

Initially

```text
{}
```

---

# 📖 Built-in Functions

---

## ➜ put(key,value)

Insert element.

```java
map.put(101,"Prince");
map.put(102,"Rahul");
map.put(103,"Aman");
```

Output

```text
{101=Prince, 102=Rahul, 103=Aman}
```

---

## Duplicate Key

```java
map.put(101,"Akash");
```

Output

```text
{101=Akash,102=Rahul,103=Aman}
```

Old value gets replaced.

---

## ➜ get(key)

```java
System.out.println(map.get(102));
```

Output

```text
Rahul
```

---

## ➜ getOrDefault()

```java
System.out.println(map.getOrDefault(105,"Not Found"));
```

Output

```text
Not Found
```

---

## ➜ containsKey()

```java
map.containsKey(101);
```

Output

```text
true
```

---

## ➜ containsValue()

```java
map.containsValue("Rahul");
```

---

## ➜ remove(key)

```java
map.remove(101);
```

---

## ➜ replace()

```java
map.replace(102,"Amit");
```

---

## ➜ size()

```java
map.size();
```

---

## ➜ clear()

```java
map.clear();
```

---

## ➜ isEmpty()

```java
map.isEmpty();
```

---

# 📖 Traversing HashMap

---

## Method 1 – keySet()

```java
for(Integer key : map.keySet())
{
    System.out.println(key);
}
```

---

## Method 2 – Values

```java
for(String value : map.values())
{
    System.out.println(value);
}
```

---

## Method 3 – key and value ⭐

```java
for(Integer key : map.keySet())
{
    System.out.println(key + " " + map.get(key));
}
```

---

## Method 4 – entrySet() ⭐⭐⭐

```java
for(Map.Entry<Integer,String> entry : map.entrySet())
{
    System.out.println(entry.getKey() + " " + entry.getValue());
}
```

---

# 📖 Internal Working

Suppose we insert

```java
map.put(101,"Prince");
```

HashMap calculates

```text
Hash Function

↓

Hash Code

↓

Bucket Index

↓

Store in Bucket
```

```text
Bucket

0

1

2 ----> (101,Prince)

3

4
```

Searching

```java
map.get(101);
```

Again computes the bucket using the hash function and retrieves the value quickly.

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| put() | O(1) Average |
| get() | O(1) Average |
| remove() | O(1) Average |
| containsKey() | O(1) Average |
| containsValue() | O(n) |
| Traversal | O(n) |

> Worst case for `put()`, `get()`, and `remove()` can be O(n), but this is rare.

---

# 📖 Common Data Types

## Integer → Integer

```java
HashMap<Integer,Integer> map = new HashMap<>();
```

---

## Integer → String

```java
HashMap<Integer,String> map = new HashMap<>();
```

---

## String → Integer

```java
HashMap<String,Integer> map = new HashMap<>();
```

---

## Character → Integer

```java
HashMap<Character,Integer> map = new HashMap<>();
```

Very useful for Frequency Count.

---

# 📖 Frequency Count (Most Important)

Given

```text
apple
```

Output

```text
a → 1
p → 2
l → 1
e → 1
```

```java
HashMap<Character,Integer> map = new HashMap<>();

for(char ch : str.toCharArray())
{
    map.put(ch, map.getOrDefault(ch,0)+1);
}
```

---

# 📖 Beginner Practice Problems ⭐

## Easy

1. Store student names using roll number
2. Print all keys
3. Print all values
4. Search a key
5. Search a value
6. Count frequency of characters
7. Count frequency of integers
8. Find maximum frequency element
9. Count vowels
10. Count consonants

---

## Easy-Medium

11. Remove duplicate characters
12. Remove duplicate integers
13. First non-repeating character
14. First repeating character
15. Count words in a sentence
16. Most frequent word
17. Check Anagram
18. Intersection of two arrays
19. Union of two arrays
20. Count distinct elements

---

## Medium

21. Two Sum
22. Subarray Sum Equals K
23. Longest Consecutive Sequence
24. Group Anagrams
25. Top K Frequent Elements
26. Isomorphic Strings
27. Happy Number
28. Find Duplicate Number
29. Valid Sudoku
30. LRU Cache (Concept)

---

# 📖 LeetCode Problems

## 🟢 Easy

- 1. Two Sum
- 217. Contains Duplicate
- 219. Contains Duplicate II
- 242. Valid Anagram
- 349. Intersection of Two Arrays
- 383. Ransom Note
- 387. First Unique Character
- 771. Jewels and Stones

---

## 🟡 Medium

- 49. Group Anagrams
- 347. Top K Frequent Elements
- 560. Subarray Sum Equals K
- 128. Longest Consecutive Sequence
- 525. Contiguous Array
- 451. Sort Characters By Frequency
- 3. Longest Substring Without Repeating Characters
- 36. Valid Sudoku
- 438. Find All Anagrams in a String

---

## 🔴 Hard

- 76. Minimum Window Substring
- 30. Substring with Concatenation of All Words
- 460. LFU Cache
- 895. Maximum Frequency Stack

---

# 📖 Common Interview Questions

1. Difference between HashMap and HashSet?
2. Difference between HashMap and TreeMap?
3. Can HashMap store duplicate keys?
4. Can HashMap store duplicate values?
5. Why is searching O(1)?
6. What is a Hash Function?
7. What is a Bucket?
8. What happens if two keys have the same hash?
9. Difference between containsKey() and containsValue()?
10. Why are immutable objects (like String) preferred as keys?

---

# 📖 HashMap vs ArrayList

| Feature | ArrayList | HashMap |
|----------|-----------|----------|
| Stores | Values | Key-Value Pairs |
| Index Based | ✅ | ❌ |
| Search | O(n) | O(1) Average |
| Duplicate Keys | N/A | ❌ |
| Duplicate Values | N/A | ✅ |
| Order | Maintained | Not Guaranteed |

---

# 📖 Real World Applications

- Phone Contacts
- Dictionary
- Student Database
- Banking Records
- Product Catalog
- Login System
- Word Frequency Counter
- Caching
- DNS Lookup
- Compiler Symbol Table

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction
- Key-Value Pair
- Real-Life Examples
- Creating HashMap
- put()
- get()
- containsKey()
- remove()
- size()
- Traversal
- Beginner Problems

---

## 🟡 Lecture 2

- getOrDefault()
- replace()
- keySet()
- values()
- entrySet()
- Frequency Count
- Time Complexity
- Internal Working
- Intermediate Problems

---

## 🔴 Lecture 3

- Collision (Concept)
- Hash Function
- Buckets
- Interview Questions
- LeetCode Problems
- HashMap vs HashSet
- HashMap vs TreeMap