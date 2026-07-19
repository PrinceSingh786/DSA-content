# 📚 Java Collections Framework – Deque (ArrayDeque)

> **Language:** Java  
> **Prerequisite:** Queue, Stack, LinkedList  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a Deque?

A **Deque (Double Ended Queue)** is a linear data structure in which insertion and deletion can happen from **both ends**.

> **Deque = Double Ended Queue**

Unlike Queue, where insertion is only at the rear and deletion is only at the front, a Deque allows operations at **both the front and the rear**.

---

# 📖 Real-Life Examples

## 🚗 Cars Entering a Parking Lane

```text
Front                          Rear

🚗  🚙  🚕  🚓
```

Cars can enter or leave from both ends.

---

## 🎴 Deck of Cards

Cards can be added or removed from either the top or bottom.

---

## 🎮 Sliding Window Problems

The Deque keeps useful elements at both ends while processing an array.

---

# 📖 Queue vs Deque

| Queue | Deque |
|--------|-------|
| Insert at Rear | Insert at Front & Rear |
| Delete from Front | Delete from Front & Rear |
| FIFO | FIFO + LIFO |
| One End Used | Two Ends Used |

---

# 📖 Stack vs Deque

| Stack | Deque |
|--------|-------|
| One End Used | Both Ends Used |
| LIFO | Can act as Stack or Queue |
| push(), pop() | addFirst(), removeFirst() |

---

# 📖 Why use Deque?

A Deque can behave like both:

- ✅ Queue (FIFO)
- ✅ Stack (LIFO)

So one data structure can replace both.

---

# 📖 Java Implementation

Java provides

```java
ArrayDeque
```

It is faster than:

- Stack
- LinkedList (for Queue operations)

---

# 📖 Import Statement

```java
import java.util.ArrayDeque;
```

or

```java
import java.util.*;
```

---

# 📖 Creating a Deque

```java
Deque<Integer> dq = new ArrayDeque<>();
```

Initially

```text
[]
```

---

# 📖 Built-in Methods

---

## ➜ addFirst()

Insert at front.

```java
dq.addFirst(20);
dq.addFirst(10);
```

Output

```text
[10,20]
```

---

## ➜ addLast()

Insert at rear.

```java
dq.addLast(30);
dq.addLast(40);
```

Output

```text
[10,20,30,40]
```

---

## ➜ offerFirst()

Same as addFirst(), but returns `false` instead of throwing an exception if insertion fails.

```java
dq.offerFirst(5);
```

---

## ➜ offerLast()

```java
dq.offerLast(50);
```

---

## ➜ removeFirst()

Removes first element.

```java
dq.removeFirst();
```

Before

```text
[10,20,30]
```

After

```text
[20,30]
```

---

## ➜ removeLast()

```java
dq.removeLast();
```

Before

```text
[20,30]
```

After

```text
[20]
```

---

## ➜ pollFirst()

Removes and returns first element.

Returns `null` if empty.

```java
dq.pollFirst();
```

---

## ➜ pollLast()

```java
dq.pollLast();
```

---

## ➜ getFirst()

Returns first element.

```java
dq.getFirst();
```

---

## ➜ getLast()

```java
dq.getLast();
```

---

## ➜ peekFirst()

Returns first element without removing it.

Returns `null` if empty.

```java
dq.peekFirst();
```

---

## ➜ peekLast()

```java
dq.peekLast();
```

---

## ➜ contains()

```java
dq.contains(20);
```

---

## ➜ size()

```java
dq.size();
```

---

## ➜ clear()

```java
dq.clear();
```

---

## ➜ isEmpty()

```java
dq.isEmpty();
```

---

# 📖 Using Deque as a Stack

```java
Deque<Integer> stack = new ArrayDeque<>();

stack.push(10);
stack.push(20);
stack.push(30);

System.out.println(stack.pop());

System.out.println(stack.peek());
```

Output

```text
30
20
```

---

# 📖 Using Deque as a Queue

```java
Deque<Integer> queue = new ArrayDeque<>();

queue.offer(10);
queue.offer(20);
queue.offer(30);

System.out.println(queue.poll());

System.out.println(queue.peek());
```

Output

```text
10
20
```

---

# 📖 Traversing Deque

## Enhanced For Loop

```java
for(int x : dq)
{
    System.out.println(x);
}
```

---

## Iterator

```java
Iterator<Integer> it = dq.iterator();

while(it.hasNext())
{
    System.out.println(it.next());
}
```

---

## Descending Iterator

```java
Iterator<Integer> it = dq.descendingIterator();

while(it.hasNext())
{
    System.out.println(it.next());
}
```

---

# 📖 Internal Working

Suppose we perform

```text
addFirst(20)

addLast(30)

addFirst(10)

addLast(40)
```

Result

```text
Front

↓

10 ← 20 ← 30 ← 40

                     ↑

                  Rear
```

Remove First

```text
20 ← 30 ← 40
```

Remove Last

```text
20 ← 30
```

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| addFirst() | O(1) |
| addLast() | O(1) |
| removeFirst() | O(1) |
| removeLast() | O(1) |
| peekFirst() | O(1) |
| peekLast() | O(1) |
| contains() | O(n) |
| size() | O(1) |

---

# 📖 ArrayDeque vs Stack

| Stack | ArrayDeque |
|--------|------------|
| Older Class | Modern Class |
| Slower | Faster |
| Synchronized | Not Synchronized |
| LIFO | LIFO |

---

# 📖 ArrayDeque vs LinkedList

| ArrayDeque | LinkedList |
|-------------|------------|
| Faster | Slightly Slower |
| Less Memory | More Memory |
| No null values | Allows null |
| Better for Queue & Stack | General-purpose List |

---

# 📖 Applications

- Browser History
- Undo / Redo
- Sliding Window
- BFS
- DFS
- Task Scheduling
- CPU Scheduling
- LRU Cache
- Expression Evaluation

---

# 📖 Beginner Practice Problems ⭐

## Easy

1. Insert at front
2. Insert at rear
3. Delete from front
4. Delete from rear
5. Print first element
6. Print last element
7. Check empty
8. Print size
9. Search element
10. Traverse Deque

---

## Easy-Medium

11. Reverse a Queue
12. Reverse first K elements
13. Implement Stack using Deque
14. Implement Queue using Deque
15. Rotate Deque
16. Merge two Deques
17. Remove duplicates
18. Find maximum element
19. Find minimum element
20. Reverse Deque

---

## Medium

21. Sliding Window Maximum
22. Sliding Window Minimum
23. First Negative Integer in Every Window
24. Circular Queue
25. Design Circular Deque
26. Shortest Subarray with Sum at Least K
27. Jump Game VI
28. Constrained Subsequence Sum
29. Maximum Robots Within Budget
30. Monotonic Queue Problems

---

# 📖 LeetCode Problems

## 🟢 Easy

- 933. Number of Recent Calls
- 225. Implement Stack using Queues
- 232. Implement Queue using Stacks

---

## 🟡 Medium

- 239. Sliding Window Maximum
- 641. Design Circular Deque
- 862. Shortest Subarray with Sum at Least K
- 1696. Jump Game VI
- 1425. Constrained Subsequence Sum

---

## 🔴 Hard

- 239. Sliding Window Maximum
- 1499. Max Value of Equation
- 1438. Longest Continuous Subarray with Absolute Difference Less Than or Equal to Limit

---

# 📖 Common Interview Questions

1. What is a Deque?
2. Difference between Queue and Deque?
3. Difference between Stack and Deque?
4. Why is ArrayDeque preferred over Stack?
5. Why doesn't ArrayDeque allow null?
6. Difference between addFirst() and offerFirst()?
7. Difference between removeFirst() and pollFirst()?
8. Difference between getFirst() and peekFirst()?
9. Time complexity of Deque operations?
10. Applications of Deque?

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction
- Queue vs Deque
- Stack vs Deque
- Creating Deque
- addFirst()
- addLast()
- removeFirst()
- removeLast()
- peekFirst()
- peekLast()
- Traversal
- Beginner Problems

---

## 🟡 Lecture 2

- offerFirst()
- offerLast()
- pollFirst()
- pollLast()
- Using Deque as Stack
- Using Deque as Queue
- Internal Working
- Time Complexity
- Intermediate Problems

---

## 🔴 Lecture 3

- Monotonic Queue
- Sliding Window Maximum
- Circular Deque
- Interview Questions
- LeetCode Problems
- Real-world Applications

---

# 📖 Key Takeaways

✅ Deque means **Double Ended Queue**.

✅ Insertion and deletion are possible from **both ends**.

✅ `ArrayDeque` is generally **faster than Stack and LinkedList** for stack and queue operations.

✅ Basic operations (`addFirst`, `addLast`, `removeFirst`, `removeLast`, `peekFirst`, `peekLast`) are **O(1)**.

✅ Deque is heavily used in:

- Sliding Window Problems
- Monotonic Queue
- BFS
- DFS
- LRU Cache
- Task Scheduling
- Expression Evaluation
- Browser History