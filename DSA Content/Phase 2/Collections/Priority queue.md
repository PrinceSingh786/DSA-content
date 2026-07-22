# 📚 Java Collections Framework – PriorityQueue (Heap)

> **Language:** Java  
> **Prerequisite:** Arrays, Queue, Comparator  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a PriorityQueue?

A **PriorityQueue** is a special type of Queue where elements are removed according to **priority**, not according to insertion order.

Unlike a normal Queue (FIFO),

- Queue → First In First Out
- PriorityQueue → Highest/Lowest Priority First

In Java,

- By default → **Min Heap**
- Can also be converted into **Max Heap**

---

# 📖 Real-Life Examples

## 🏥 Hospital Emergency Room

```text
Patient A (Critical)
Patient B (Normal)
Patient C (Emergency)
Patient D (Minor Injury)
```

Treatment Order

```text
Patient A

↓

Patient C

↓

Patient B

↓

Patient D
```

Not based on arrival time.

---

## ✈ Airport Landing

Planes with low fuel land first.

---

## 🖥 CPU Scheduling

Higher priority processes execute first.

---

## 🎮 Online Games

Higher ranked players get priority.

---

# 📖 Queue vs PriorityQueue

| Queue | PriorityQueue |
|--------|---------------|
| FIFO | Priority Based |
| First inserted removed first | Highest/Lowest priority removed first |
| Front & Rear | Heap |
| O(1) dequeue | O(log n) dequeue |

---

# 📖 Heap

A **Heap** is a Complete Binary Tree.

Two types

## Min Heap

Smallest element remains at the top.

```text
        5
      /   \
     8     10
    / \   /
  15 20 12
```

---

## Max Heap

Largest element remains at the top.

```text
        20
      /    \
    18      15
   /  \    /
 10   12  8
```

---

# 📖 Java PriorityQueue

By default

```java
PriorityQueue<Integer> pq = new PriorityQueue<>();
```

Creates a **Min Heap**.

---

# 📖 Import Statement

```java
import java.util.PriorityQueue;
```

or

```java
import java.util.*;
```

---

# 📖 Creating a PriorityQueue

## Min Heap

```java
PriorityQueue<Integer> pq = new PriorityQueue<>();
```

---

## Max Heap

```java
PriorityQueue<Integer> pq =
new PriorityQueue<>(Collections.reverseOrder());
```

---

# 📖 Built-in Methods

---

## ➜ offer()

Insert element.

```java
pq.offer(30);
pq.offer(10);
pq.offer(20);
```

Heap

```text
10
20
30
```

---

## ➜ add()

Same as offer().

```java
pq.add(40);
```

---

## ➜ poll()

Removes highest priority element.

```java
pq.poll();
```

Output

```text
10
```

Remaining

```text
20
30
40
```

---

## ➜ remove()

```java
pq.remove();
```

Removes highest priority element.

---

## ➜ peek()

Returns top element.

```java
pq.peek();
```

Output

```text
20
```

---

## ➜ contains()

```java
pq.contains(30);
```

---

## ➜ size()

```java
pq.size();
```

---

## ➜ clear()

```java
pq.clear();
```

---

## ➜ isEmpty()

```java
pq.isEmpty();
```

---

# 📖 Traversing PriorityQueue

## Enhanced For Loop

```java
for(int x : pq)
{
    System.out.println(x);
}
```

> ⚠ **Important:** Traversing does **NOT** print elements in sorted order.

---

## Poll Until Empty ⭐

```java
while(!pq.isEmpty())
{
    System.out.println(pq.poll());
}
```

Output

```text
10
20
30
40
50
```

Always sorted according to priority.

---

# 📖 Internal Working

Insert

```text
30
```

Heap

```text
30
```

---

Insert

```text
10
```

```text
30
/
10
```

Swap

```text
10
/
30
```

---

Insert

```text
20
```

```text
      10
     /  \
   30   20
```

Heap property maintained.

---

Insert

```text
5
```

```text
       5
     /   \
   10     20
  /
30
```

---

# 📖 Min Heap Example

Insert

```text
40
30
20
10
50
```

Heap becomes

```text
        10
      /    \
    20      30
   /  \
 40   50
```

---

# 📖 Max Heap Example

```java
PriorityQueue<Integer> pq =
new PriorityQueue<>(Collections.reverseOrder());
```

Insert

```text
40
30
20
10
50
```

Heap

```text
        50
      /    \
    40      20
   /  \
 10   30
```

---

# 📖 Custom Priority (Comparator)

Sort Strings by Length

```java
PriorityQueue<String> pq =
new PriorityQueue<>(
(a,b)->a.length()-b.length()
);
```

---

Sort Students by Marks

```java
PriorityQueue<Student> pq =
new PriorityQueue<>(
(a,b)->b.marks-a.marks
);
```

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| offer() | O(log n) |
| add() | O(log n) |
| poll() | O(log n) |
| remove() | O(log n) |
| peek() | O(1) |
| size() | O(1) |
| contains() | O(n) |

---

# 📖 PriorityQueue vs Queue

| Queue | PriorityQueue |
|--------|---------------|
| FIFO | Priority Based |
| O(1) Poll | O(log n) Poll |
| LinkedList | Heap |
| Arrival Order | Priority Order |

---

# 📖 PriorityQueue vs TreeSet

| PriorityQueue | TreeSet |
|---------------|----------|
| Duplicate Elements Allowed | No Duplicates |
| Only Top Accessible | Full Sorted Order |
| Heap | Red Black Tree |
| O(log n) | O(log n) |

---

# 📖 Applications

- CPU Scheduling
- Dijkstra Algorithm
- Prim's Algorithm
- Huffman Coding
- A* Search
- Merge K Sorted Lists
- Kth Largest Element
- Top K Frequent Elements
- Streaming Median
- Task Scheduling

---

# 📖 Beginner Practice Problems ⭐

## Easy

1. Insert N elements
2. Print smallest element
3. Remove smallest element
4. Print size
5. Check empty
6. Find maximum (without removing)
7. Find minimum
8. Insert duplicate elements
9. Traverse PriorityQueue
10. Convert array into PriorityQueue

---

## Easy-Medium

11. Kth Smallest Element
12. Kth Largest Element
13. Last Stone Weight
14. Merge K Sorted Arrays
15. Connect Ropes with Minimum Cost
16. Sort Nearly Sorted Array
17. Find Top K Largest Elements
18. Running Median
19. Reorganize String
20. Task Scheduler

---

## Medium

21. Top K Frequent Elements
22. K Closest Points to Origin
23. Find K Pairs with Smallest Sums
24. IPO
25. Meeting Rooms II
26. Furthest Building You Can Reach
27. Seat Reservation Manager
28. Single Threaded CPU
29. Minimum Cost to Hire Workers
30. Sliding Window Median

---

# 📖 LeetCode Problems

## 🟢 Easy

- 1046. Last Stone Weight
- 703. Kth Largest Element in a Stream
- 506. Relative Ranks

---

## 🟡 Medium

- 215. Kth Largest Element in an Array
- 347. Top K Frequent Elements
- 973. K Closest Points to Origin
- 378. Kth Smallest Element in a Sorted Matrix
- 1167. Minimum Cost to Connect Sticks
- 1834. Single-Threaded CPU
- 2402. Meeting Rooms III

---

## 🔴 Hard

- 23. Merge K Sorted Lists
- 295. Find Median from Data Stream
- 480. Sliding Window Median
- 502. IPO
- 632. Smallest Range Covering Elements from K Lists

---

# 📖 Common Interview Questions

1. What is a PriorityQueue?
2. Difference between Queue and PriorityQueue?
3. What is a Heap?
4. Difference between Min Heap and Max Heap?
5. Why is peek() O(1)?
6. Why is offer() O(log n)?
7. How do we create a Max Heap?
8. Can PriorityQueue store duplicate elements?
9. Can PriorityQueue store null?
10. Difference between TreeSet and PriorityQueue?

---

# 📖 Real-World Applications

- Hospital Management
- Flight Scheduling
- CPU Scheduling
- Operating Systems
- Graph Algorithms
- Search Engines
- Online Gaming
- Streaming Data
- Event Processing
- Network Routing

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction
- Queue vs PriorityQueue
- Heap Concept
- Min Heap
- Creating PriorityQueue
- offer()
- poll()
- peek()
- Traversal
- Beginner Problems

---

## 🟡 Lecture 2

- Max Heap
- Comparator
- Internal Working
- Heapify Concept
- Time Complexity
- Intermediate Problems

---

## 🔴 Lecture 3

- Kth Largest
- Top K Frequent
- Merge K Lists
- Dijkstra (Introduction)
- Prim's Algorithm (Introduction)
- Interview Questions
- LeetCode Problems

---

# 📖 Key Takeaways

✅ PriorityQueue is implemented using a **Binary Heap**.

✅ By default, Java's PriorityQueue is a **Min Heap**.

✅ Use `Collections.reverseOrder()` to create a **Max Heap**.

✅ Basic complexities:

- `offer()` → **O(log n)**
- `poll()` → **O(log n)**
- `peek()` → **O(1)**

✅ PriorityQueue is widely used in:

- Dijkstra's Algorithm
- Prim's Algorithm
- Huffman Coding
- Kth Largest/Smallest Problems
- Top K Frequent Elements
- Task Scheduling
- Streaming Data
- CPU Scheduling
```