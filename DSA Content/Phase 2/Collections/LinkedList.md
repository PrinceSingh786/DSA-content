# 🔗 Java Collections Framework – LinkedList

> **Language:** Java  
> **Prerequisite:** Arrays, ArrayList, Loops, Functions  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a LinkedList?

A **LinkedList** is a linear data structure where elements are stored in **nodes**.

Each node contains:

- 📦 Data
- 👉 Address (Reference) of the next node

Unlike an ArrayList, elements are **not stored in contiguous memory**.

---

# 📖 Visual Representation

```text
┌─────┬─────┐     ┌─────┬─────┐     ┌─────┬──────┐
│ 10  │  ●──┼────▶│ 20  │  ●──┼────▶│ 30  │ NULL │
└─────┴─────┘     └─────┴─────┘     └─────┴──────┘
```

Every box is called a **Node**.

---

# 📖 Why do we need LinkedList?

Suppose we have

```text
10 20 30 40
```

Now insert **25**.

### ArrayList

```text
10 20 30 40

↓

Shift 30
Shift 40

↓

10 20 25 30 40
```

Many elements need shifting.

---

### LinkedList

```text
10 → 20 → 30 → 40

↓

10 → 20 → 25 → 30 → 40
```

Only pointers are changed.

No shifting.

---

# 📖 ArrayList vs LinkedList

| Feature | ArrayList | LinkedList |
|----------|-----------|------------|
| Storage | Dynamic Array | Nodes |
| Random Access | ✅ O(1) | ❌ O(n) |
| Insert Beginning | ❌ O(n) | ✅ O(1) |
| Delete Beginning | ❌ O(n) | ✅ O(1) |
| Memory Usage | Less | More |
| Searching | O(n) | O(n) |

---

# 📖 Import Statement

```java
import java.util.LinkedList;
```

or

```java
import java.util.*;
```

---

# 📖 Creating a LinkedList

```java
LinkedList<Integer> list = new LinkedList<>();
```

---

# 📖 Printing LinkedList

```java
System.out.println(list);
```

Output

```text
[]
```

---

# 📖 Adding Elements

## ➜ add()

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

## ➜ addFirst()

```java
list.addFirst(5);
```

Output

```text
[5, 10, 20, 30]
```

---

## ➜ addLast()

```java
list.addLast(40);
```

Output

```text
[5, 10, 20, 30, 40]
```

---

## ➜ add(index, value)

```java
list.add(2,100);
```

Output

```text
[5, 10, 100, 20, 30, 40]
```

---

# 📖 Accessing Elements

## ➜ get(index)

```java
list.get(2);
```

---

## ➜ getFirst()

```java
list.getFirst();
```

---

## ➜ getLast()

```java
list.getLast();
```

---

# 📖 Updating Elements

## ➜ set(index, value)

```java
list.set(1,500);
```

---

# 📖 Removing Elements

## ➜ remove()

Removes first element.

```java
list.remove();
```

---

## ➜ remove(index)

```java
list.remove(2);
```

---

## ➜ remove(Object)

```java
list.remove(Integer.valueOf(20));
```

---

## ➜ removeFirst()

```java
list.removeFirst();
```

---

## ➜ removeLast()

```java
list.removeLast();
```

---

# 📖 Searching

## ➜ contains()

```java
list.contains(30);
```

---

## ➜ indexOf()

```java
list.indexOf(30);
```

---

## ➜ lastIndexOf()

```java
list.lastIndexOf(30);
```

---

# 📖 Other Useful Methods

## ➜ size()

```java
list.size();
```

---

## ➜ clear()

```java
list.clear();
```

---

## ➜ isEmpty()

```java
list.isEmpty();
```

---

# 📖 Collections Utility Methods

## Sort

```java
Collections.sort(list);
```

---

## Reverse

```java
Collections.reverse(list);
```

---

## Shuffle

```java
Collections.shuffle(list);
```

---

## Maximum

```java
Collections.max(list);
```

---

## Minimum

```java
Collections.min(list);
```

---

## Frequency

```java
Collections.frequency(list,10);
```

---

# 📖 Traversing LinkedList

---

## Method 1 – For Loop

```java
for(int i=0;i<list.size();i++)
{
    System.out.println(list.get(i));
}
```

> ⚠️ This works but is slower because every `get(i)` takes O(n).

---

## Method 2 – Enhanced For Loop ⭐

```java
for(int x:list)
{
    System.out.println(x);
}
```

---

## Method 3 – Iterator ⭐⭐⭐

```java
Iterator<Integer> it = list.iterator();

while(it.hasNext())
{
    System.out.println(it.next());
}
```

---

# 📖 Internal Working

Suppose we have

```text
10 → 20 → 30 → 40
```

Internally

```text
┌──────┬────────┐
│  10  │   ●────┼────────────┐
└──────┴────────┘            │
                             ▼
                     ┌──────┬────────┐
                     │  20  │   ●────┼──────────┐
                     └──────┴────────┘          │
                                                ▼
                                        ┌──────┬────────┐
                                        │  30  │   ●────┼─────┐
                                        └──────┴────────┘     │
                                                              ▼
                                                      ┌──────┬──────┐
                                                      │  40  │ NULL │
                                                      └──────┴──────┘
```

Each node stores

- Data
- Reference to next node

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| addFirst() | O(1) |
| addLast() | O(1) |
| removeFirst() | O(1) |
| removeLast() | O(1) |
| get(index) | O(n) |
| set(index) | O(n) |
| contains() | O(n) |
| add(index) | O(n) |
| remove(index) | O(n) |

---

# 📖 Beginner Practice Problems ⭐

## Easy

1. Print all elements
2. Find sum
3. Find maximum
4. Find minimum
5. Count even numbers
6. Count odd numbers
7. Search an element
8. Reverse printing
9. Count frequency of a value
10. Replace negative numbers with zero

---

## Easy-Medium

11. Remove even numbers
12. Remove odd numbers
13. Copy LinkedList
14. Merge two LinkedLists
15. Find second largest
16. Find second smallest
17. Reverse the LinkedList
18. Remove duplicates
19. Rotate left
20. Rotate right

---

## Medium

21. Move zeros to end
22. Check palindrome
23. Find middle element
24. Remove nth node from end
25. Merge sorted LinkedLists
26. Detect cycle (concept only)
27. Reverse in groups
28. Partition list
29. Delete duplicates from sorted list
30. Rearrange odd-even nodes

---

# 📖 LeetCode Problems

## 🟢 Easy

- 206. Reverse Linked List
- 21. Merge Two Sorted Lists
- 83. Remove Duplicates from Sorted List
- 203. Remove Linked List Elements
- 876. Middle of the Linked List
- 141. Linked List Cycle

---

## 🟡 Medium

- 2. Add Two Numbers
- 19. Remove Nth Node From End
- 24. Swap Nodes in Pairs
- 61. Rotate List
- 86. Partition List
- 92. Reverse Linked List II
- 143. Reorder List
- 328. Odd Even Linked List
- 142. Linked List Cycle II

---

## 🔴 Hard

- 23. Merge K Sorted Lists
- 25. Reverse Nodes in K Group
- 460. LFU Cache
- 432. All O(1) Data Structure

---

# 📖 Common Interview Questions

1. Difference between ArrayList and LinkedList?
2. Why is `get(index)` slow?
3. Why is insertion at the beginning O(1)?
4. Why does LinkedList use more memory?
5. What is a Node?
6. Difference between Singly and Doubly LinkedList?
7. Difference between `addFirst()` and `add()`?
8. Difference between `remove()` and `removeFirst()`?
9. Why is random access slow?
10. When should we use LinkedList?

---

# 📖 ArrayList vs LinkedList

| Operation | ArrayList | LinkedList |
|------------|-----------|------------|
| get(i) | ✅ O(1) | ❌ O(n) |
| addLast() | ✅ O(1) Amortized | ✅ O(1) |
| addFirst() | ❌ O(n) | ✅ O(1) |
| removeFirst() | ❌ O(n) | ✅ O(1) |
| removeLast() | ✅ O(1) | ✅ O(1) |
| Insert Middle | O(n) | O(n) |
| Memory | Less | More |

---

# 📖 When Should We Use LinkedList?

✅ Frequent insertions and deletions

Examples:

- Music Playlist
- Browser History
- Undo/Redo
- Queue
- Stack
- LRU Cache
- Task Scheduler

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction
- What is a Node?
- Internal Working
- Creating LinkedList
- add()
- addFirst()
- addLast()
- get()
- set()
- remove()
- Traversal
- Beginner Problems

---

## 🟡 Lecture 2

- contains()
- indexOf()
- lastIndexOf()
- clear()
- size()
- Collections methods
- Time Complexity
- ArrayList vs LinkedList
- Intermediate Problems

---

## 🔴 Lecture 3

- Interview Questions
- Real-world Applications
- LeetCode Problems
- Introduction to Custom Linked List (Node class)
- Singly vs Doubly vs Circular Linked List