# 🌳 Java Collections Framework – TreeSet

> **Language:** Java  
> **Prerequisite:** HashSet, Comparable, Comparator (Basic Idea)  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a TreeSet?

A **TreeSet** is a collection that stores **unique elements in sorted order**.

Unlike HashSet,

- ✅ Elements are always sorted
- ✅ Duplicate elements are not allowed
- ✅ Fast searching
- ❌ No indexing

Internally, TreeSet uses a **Red-Black Tree (Self-Balancing BST).**

---

# 📖 Real-Life Examples

## 📚 Dictionary

```text
Apple
Banana
Cat
Dog
Elephant
```

Words are always stored alphabetically.

---

## 🎓 Student Roll Numbers

```text
101
102
103
104
105
```

Always sorted.

---

## 🌍 Countries

```text
Australia
India
Japan
USA
```

Automatically sorted.

---

# 📖 Why TreeSet?

Suppose we insert

```text
50
20
10
40
30
```

HashSet

```text
20 50 10 30 40
```

(Random Order)

TreeSet

```text
10 20 30 40 50
```

(Automatically Sorted)

---

# 📖 HashSet vs TreeSet

| HashSet | TreeSet |
|----------|----------|
| Random Order | Sorted Order |
| Hash Table | Red Black Tree |
| O(1) Search | O(log n) Search |
| No Ordering | Natural Ordering |

---

# 📖 Import Statement

```java
import java.util.TreeSet;
```

or

```java
import java.util.*;
```

---

# 📖 Creating TreeSet

```java
TreeSet<Integer> set = new TreeSet<>();
```

---

# 📖 Built-in Methods

---

## ➜ add()

```java
set.add(30);
set.add(10);
set.add(20);
```

Output

```text
[10,20,30]
```

---

## Duplicate

```java
set.add(20);
```

Nothing happens.

---

## ➜ remove()

```java
set.remove(20);
```

---

## ➜ contains()

```java
set.contains(30);
```

---

## ➜ first()

Returns smallest element.

```java
set.first();
```

---

## ➜ last()

Returns largest element.

```java
set.last();
```

---

## ➜ higher()

Smallest element greater than given value.

```java
set.higher(30);
```

---

## ➜ lower()

Largest element smaller than given value.

```java
set.lower(30);
```

---

## ➜ ceiling()

Smallest element ≥ x

```java
set.ceiling(30);
```

---

## ➜ floor()

Largest element ≤ x

```java
set.floor(30);
```

---

## ➜ pollFirst()

Removes smallest element.

```java
set.pollFirst();
```

---

## ➜ pollLast()

Removes largest element.

```java
set.pollLast();
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

# 📖 Traversing TreeSet

## Enhanced For Loop

```java
for(int x : set)
{
    System.out.println(x);
}
```

---

## Iterator

```java
Iterator<Integer> it = set.iterator();

while(it.hasNext())
{
    System.out.println(it.next());
}
```

---

## Descending Order

```java
Iterator<Integer> it =
set.descendingIterator();

while(it.hasNext())
{
    System.out.println(it.next());
}
```

---

# 📖 Internal Working

Insert

```text
30
20
40
10
50
```

Tree

```text
        30
       /  \
     20    40
    /        \
   10        50
```

TreeSet balances itself automatically.

Internally uses

```text
Red Black Tree
```

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| add() | O(log n) |
| remove() | O(log n) |
| contains() | O(log n) |
| first() | O(log n) |
| last() | O(log n) |
| higher() | O(log n) |
| lower() | O(log n) |

---

# 📖 HashSet vs TreeSet

| Feature | HashSet | TreeSet |
|----------|----------|----------|
| Duplicate | ❌ | ❌ |
| Sorted | ❌ | ✅ |
| Search | O(1) | O(log n) |
| Internal DS | Hash Table | Red Black Tree |

---

# 📖 Applications

- Leaderboard
- Dictionary
- Auto Complete
- Ranking Systems
- Floor & Ceiling Queries
- Scheduling
- Booking Systems

---

# 📖 Beginner Problems ⭐

1. Insert N elements
2. Remove duplicates
3. Print sorted elements
4. Print smallest element
5. Print largest element
6. Find floor
7. Find ceiling
8. Find higher
9. Find lower
10. Reverse traversal

---

# 📖 Medium Problems

11. Leaderboard
12. Nearby Duplicate
13. Longest Consecutive Sequence (TreeSet)
14. Calendar Booking
15. Exam Room
16. Contains Nearby Almost Duplicate
17. Sliding Window Median
18. Skyline Problem
19. Data Stream
20. Ordered Stream

---

# 📖 LeetCode Problems

## 🟢 Easy

- 2206. Divide Array Into Equal Pairs
- 414. Third Maximum Number

## 🟡 Medium

- 729. My Calendar I
- 855. Exam Room
- 220. Contains Duplicate III

## 🔴 Hard

- 480. Sliding Window Median
- 352. Data Stream as Disjoint Intervals

---

# 📖 Common Interview Questions

1. Difference between HashSet and TreeSet?
2. Why is TreeSet slower?
3. Can TreeSet store duplicate elements?
4. Can TreeSet store null?
5. What is Natural Ordering?
6. What is Red Black Tree?
7. Difference between higher() and ceiling()?
8. Difference between lower() and floor()?
9. Why are operations O(log n)?
10. When should we use TreeSet?

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction
- HashSet vs TreeSet
- Creating TreeSet
- add()
- remove()
- contains()
- first()
- last()
- Traversal
- Beginner Problems

---

## 🟡 Lecture 2

- higher()
- lower()
- floor()
- ceiling()
- pollFirst()
- pollLast()
- Internal Working
- Time Complexity
- Applications

---

## 🔴 Lecture 3

- Red Black Tree (Basic Idea)
- TreeSet vs HashSet
- Interview Questions
- LeetCode Problems
- Introduction to TreeMap

---

# 📖 Key Takeaways

✅ TreeSet stores **unique elements**.

✅ Elements are always **sorted**.

✅ Implemented using **Red Black Tree**.

✅ All operations take **O(log n)**.

✅ Useful for:

- Floor/Ceiling Queries
- Ordered Data
- Leaderboards
- Scheduling
- Ranking Systems