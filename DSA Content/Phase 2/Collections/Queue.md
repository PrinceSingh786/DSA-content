# 📚 Java Collections Framework – Queue

> **Language:** Java  
> **Prerequisite:** Arrays, ArrayList, Stack  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a Queue?

A **Queue** is a linear data structure that follows the **FIFO** principle.

> **FIFO = First In, First Out**

The element inserted **first** is removed **first**.

---

# 📖 Real-Life Examples

## 🚶 Queue at Ticket Counter

```text
Front

👨 → 👩 → 👦 → 👴

Rear
```

The person who comes **first** gets the ticket **first**.

---

## 🏦 Bank Queue

```text
Front

Customer 1
Customer 2
Customer 3
Customer 4

Rear
```

---

## 🚌 Bus Stop Queue

First person standing gets on the bus first.

---

## 🖨️ Printer Queue

```text
Document A

↓

Document B

↓

Document C
```

The printer prints

```text
A

↓

B

↓

C
```

---

# 📖 Queue Representation

```text
           Front
             │
             ▼

┌────┬────┬────┬────┐
│10  │20  │30  │40  │
└────┴────┴────┴────┘

                    ▲
                    │
                   Rear
```

Insertion happens at **Rear**

Deletion happens at **Front**

---

# 📖 Queue Terminology

- **Enqueue** → Insert element
- **Dequeue** → Remove element
- **Peek / Front** → View front element
- **Rear** → Last element
- **isEmpty()** → Check if queue is empty

---

# 📖 Queue Interface

Queue is an **Interface**.

Common implementations are:

```text
Queue
   │
   ├── LinkedList ✅
   ├── PriorityQueue
   └── ArrayDeque ⭐ (Recommended)
```

For beginners, use **LinkedList**.

---

# 📖 Import Statement

```java
import java.util.Queue;
import java.util.LinkedList;
```

or

```java
import java.util.*;
```

---

# 📖 Creating a Queue

```java
Queue<Integer> queue = new LinkedList<>();
```

Initially

```text
[]
```

---

# 📖 Built-in Functions

---

## ➜ offer()

Insert element.

```java
queue.offer(10);
queue.offer(20);
queue.offer(30);
```

Output

```text
[10, 20, 30]
```

---

## ➜ poll()

Removes front element.

```java
queue.poll();
```

Before

```text
[10,20,30]
```

After

```text
[20,30]
```

Removed

```text
10
```

---

## ➜ peek()

Returns front element.

```java
System.out.println(queue.peek());
```

Output

```text
20
```

---

## ➜ isEmpty()

```java
queue.isEmpty();
```

---

## ➜ size()

```java
queue.size();
```

---

## ➜ contains()

```java
queue.contains(30);
```

---

## ➜ clear()

```java
queue.clear();
```

---

# 📖 Traversing Queue

---

## Method 1 – Enhanced For Loop

```java
for(int x : queue)
{
    System.out.println(x);
}
```

---

## Method 2 – Iterator

```java
Iterator<Integer> it = queue.iterator();

while(it.hasNext())
{
    System.out.println(it.next());
}
```

---

## Method 3 – Poll Until Empty ⭐

```java
while(!queue.isEmpty())
{
    System.out.println(queue.poll());
}
```

---

# 📖 Internal Working

Initially

```text
Front Rear

[]
```

Offer 10

```text
Front Rear

[10]
```

Offer 20

```text
Front        Rear

[10] [20]
```

Offer 30

```text
Front             Rear

[10] [20] [30]
```

Poll

```text
10 removed

Front      Rear

[20] [30]
```

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| offer() | O(1) |
| poll() | O(1) |
| peek() | O(1) |
| size() | O(1) |
| isEmpty() | O(1) |
| contains() | O(n) |

---

# 📖 Queue vs Stack

| Queue | Stack |
|--------|--------|
| FIFO | LIFO |
| offer() | push() |
| poll() | pop() |
| peek() | peek() |
| Insert at Rear | Insert at Top |
| Remove from Front | Remove from Top |

---

# 📖 Queue vs ArrayList

| Queue | ArrayList |
|--------|-----------|
| FIFO | Random Access |
| No Indexing | Index Based |
| Front & Rear | Index |
| Fast Removal from Front | Slow Removal from Front |

---

# 📖 Queue vs LinkedList

| Queue | LinkedList |
|--------|------------|
| Interface | Class |
| FIFO Operations | General List Operations |
| offer(), poll(), peek() | add(), remove(), get() |

---

# 📖 Beginner Practice Problems ⭐

## Easy

1. Insert N elements
2. Remove one element
3. Print front element
4. Print queue
5. Check if queue is empty
6. Print size
7. Search an element
8. Count even numbers
9. Count odd numbers
10. Find maximum element

---

## Easy-Medium

11. Reverse a Queue
12. Reverse first K elements
13. Generate Binary Numbers
14. Interleave First Half
15. Copy Queue
16. Merge Two Queues
17. Remove duplicates
18. Print Queue without modifying it
19. Find minimum element
20. Rotate Queue

---

# 📖 Medium Problems

21. Implement Stack using Queue
22. Circular Queue
23. Sliding Window Maximum
24. Rotten Oranges
25. Number of Recent Calls
26. First Non-Repeating Character
27. Moving Average from Data Stream
28. Time Needed to Buy Tickets
29. Dota2 Senate
30. Reveal Cards in Increasing Order

---

# 📖 LeetCode Problems

## 🟢 Easy

- 232. Implement Queue using Stacks
- 933. Number of Recent Calls
- 1700. Number of Students Unable to Eat Lunch
- 225. Implement Stack using Queues

---

## 🟡 Medium

- 994. Rotten Oranges
- 649. Dota2 Senate
- 622. Design Circular Queue
- 950. Reveal Cards in Increasing Order
- 346. Moving Average from Data Stream
- 239. Sliding Window Maximum (Deque)
- 649. Dota2 Senate

---

## 🔴 Hard

- 239. Sliding Window Maximum
- 862. Shortest Subarray with Sum at Least K
- 1438. Longest Continuous Subarray with Absolute Difference Less Than Limit

---

# 📖 Common Interview Questions

1. What is FIFO?
2. Difference between Queue and Stack?
3. Difference between offer() and add()?
4. Difference between poll() and remove()?
5. Difference between peek() and element()?
6. Why is Queue an interface?
7. Why do we use LinkedList for Queue?
8. Difference between Queue and Deque?
9. What is Circular Queue?
10. Real-world applications of Queue?

---

# 📖 Real-World Applications

- Ticket Booking System
- Printer Queue
- CPU Scheduling
- BFS (Breadth First Search)
- Level Order Traversal
- Call Center
- Network Packet Processing
- Order Processing
- Task Scheduling
- Streaming Systems

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction
- FIFO Principle
- Real-Life Examples
- Queue Interface
- LinkedList Implementation
- offer()
- poll()
- peek()
- size()
- isEmpty()
- Traversal
- Beginner Problems

---

## 🟡 Lecture 2

- Queue vs Stack
- Queue vs ArrayList
- Internal Working
- Time Complexity
- Reverse Queue
- Reverse First K Elements
- Applications
- Intermediate Problems

---

## 🔴 Lecture 3

- Circular Queue
- Deque (Introduction)
- Sliding Window
- BFS Concept
- Rotten Oranges
- Interview Questions
- LeetCode Problems

---

# 📖 Key Takeaways

✅ Queue follows **FIFO (First In, First Out)**.

✅ Insertion happens at the **Rear**.

✅ Deletion happens at the **Front**.

✅ Basic operations (`offer`, `poll`, `peek`) are **O(1)**.

✅ Queue is widely used in:

- BFS (Graphs & Trees)
- CPU Scheduling
- Printer Queue
- Ticket Booking Systems
- Call Centers
- Network Routing
- Task Scheduling
- Streaming Applications