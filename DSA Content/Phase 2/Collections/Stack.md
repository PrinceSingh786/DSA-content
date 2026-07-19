# 📚 Java Collections Framework – Stack

> **Language:** Java  
> **Prerequisite:** Arrays, ArrayList, Loops, Functions  
> **Difficulty:** Beginner → Intermediate

---

# 📖 What is a Stack?

A **Stack** is a linear data structure that follows the **LIFO** principle.

> **LIFO = Last In, First Out**

The element inserted **last** is removed **first**.

---

# 📖 Real-Life Examples

## 📚 Stack of Books

```text
       📕  ← Top
       📘
       📗
       📙
```

You can only remove the **top book**.

---

## 🍽️ Stack of Plates

```text
       🍽️
       🍽️
       🍽️
       🍽️
```

The last plate placed is removed first.

---

## 🌐 Browser Back Button

```text
Google

↓

YouTube

↓

LeetCode

↓

ChatGPT
```

Press Back

```text
ChatGPT removed

↓

LeetCode
```

---

## 📝 Undo in MS Word

```text
Type A

↓

Type B

↓

Type C
```

Undo removes

```text
C

↓

B

↓

A
```

---

# 📖 Stack Operations

```text
           TOP
            │
            ▼
        ┌───────┐
        │   40  │
        ├───────┤
        │   30  │
        ├───────┤
        │   20  │
        ├───────┤
        │   10  │
        └───────┘
```

Only the **Top** element can be accessed.

---

# 📖 Stack Terminology

- **Push** → Insert element
- **Pop** → Remove top element
- **Peek** → View top element
- **isEmpty()** → Check whether stack is empty

---

# 📖 Import Statement

```java
import java.util.Stack;
```

or

```java
import java.util.*;
```

---

# 📖 Creating a Stack

```java
Stack<Integer> stack = new Stack<>();
```

Initially

```text
[]
```

---

# 📖 Built-in Functions

---

## ➜ push()

Insert an element.

```java
stack.push(10);
stack.push(20);
stack.push(30);
```

Output

```text
[10, 20, 30]
```

Top = 30

---

## ➜ pop()

Removes the top element.

```java
stack.pop();
```

Before

```text
[10,20,30]
```

After

```text
[10,20]
```

Removed = 30

---

## ➜ peek()

Returns the top element.

```java
System.out.println(stack.peek());
```

Output

```text
20
```

---

## ➜ isEmpty()

```java
stack.isEmpty();
```

---

## ➜ size()

```java
stack.size();
```

---

## ➜ search()

Returns the **1-based position from the top**.

```java
stack.push(10);
stack.push(20);
stack.push(30);

System.out.println(stack.search(20));
```

Output

```text
2
```

---

## ➜ clear()

```java
stack.clear();
```

---

# 📖 Traversing Stack

---

## Method 1 – Enhanced For Loop

```java
for(int x : stack)
{
    System.out.println(x);
}
```

---

## Method 2 – Using Index

```java
for(int i = 0; i < stack.size(); i++)
{
    System.out.println(stack.get(i));
}
```

---

## Method 3 – Pop Until Empty ⭐

```java
while(!stack.isEmpty())
{
    System.out.println(stack.pop());
}
```

---

# 📖 Internal Working

Initially

```text
[]
```

Push 10

```text
TOP
 │
 ▼

┌────┐
│10  │
└────┘
```

Push 20

```text
TOP
 │
 ▼

┌────┐
│20  │
├────┤
│10  │
└────┘
```

Push 30

```text
TOP
 │
 ▼

┌────┐
│30  │
├────┤
│20  │
├────┤
│10  │
└────┘
```

Pop

```text
30 removed

TOP
 │
 ▼

┌────┐
│20  │
├────┤
│10  │
└────┘
```

---

# 📖 Time Complexity

| Operation | Complexity |
|------------|------------|
| push() | O(1) |
| pop() | O(1) |
| peek() | O(1) |
| isEmpty() | O(1) |
| size() | O(1) |
| search() | O(n) |

---

# 📖 Beginner Practice Problems ⭐

## Easy

1. Push N elements
2. Pop one element
3. Print top element
4. Check if stack is empty
5. Print size
6. Print all elements
7. Reverse a string using Stack
8. Reverse an array using Stack
9. Copy one Stack into another
10. Find maximum element

---

## Easy-Medium

11. Remove all elements
12. Print stack without modifying it
13. Count even numbers
14. Count odd numbers
15. Insert element at bottom
16. Reverse stack
17. Sort stack
18. Delete middle element
19. Remove duplicates
20. Find minimum element

---

## Medium

21. Valid Parentheses
22. Next Greater Element
23. Next Smaller Element
24. Previous Greater Element
25. Previous Smaller Element
26. Stock Span Problem
27. Daily Temperatures
28. Asteroid Collision
29. Decode String
30. Evaluate Reverse Polish Notation

---

# 📖 LeetCode Problems

## 🟢 Easy

- 20. Valid Parentheses
- 225. Implement Stack using Queues
- 232. Implement Queue using Stacks
- 844. Backspace String Compare
- 1047. Remove All Adjacent Duplicates in String

---

## 🟡 Medium

- 739. Daily Temperatures
- 496. Next Greater Element I
- 503. Next Greater Element II
- 71. Simplify Path
- 150. Evaluate Reverse Polish Notation
- 394. Decode String
- 901. Online Stock Span
- 735. Asteroid Collision

---

## 🔴 Hard

- 84. Largest Rectangle in Histogram
- 85. Maximal Rectangle
- 42. Trapping Rain Water (Stack Approach)
- 316. Remove Duplicate Letters
- 32. Longest Valid Parentheses

---

# 📖 Common Interview Questions

1. What is LIFO?
2. Difference between Stack and Queue?
3. Difference between push() and add()?
4. Difference between peek() and pop()?
5. Can we access the middle element directly?
6. What happens if we pop an empty stack?
7. Real-life applications of Stack?
8. Time complexity of push()?
9. Why is Stack useful for recursion?
10. Difference between Java Stack and ArrayDeque?

---

# 📖 Stack vs Queue

| Stack | Queue |
|--------|--------|
| LIFO | FIFO |
| push() | offer()/add() |
| pop() | poll()/remove() |
| peek() | peek() |
| One end used | Two ends used |

---

# 📖 Real-World Applications

- Browser History
- Undo / Redo
- Function Calls
- Recursion
- Expression Evaluation
- Parentheses Matching
- Syntax Checking
- Backtracking
- DFS (Depth First Search)
- Next Greater Element

---

# 📖 Teaching Order

## 🟢 Lecture 1

- Introduction to Stack
- LIFO Principle
- Real-Life Examples
- push()
- pop()
- peek()
- isEmpty()
- size()
- Traversal
- Beginner Problems

---

## 🟡 Lecture 2

- Reverse String
- Reverse Array
- Insert at Bottom
- Reverse Stack
- Internal Working
- Time Complexity
- Applications
- Intermediate Problems

---

## 🔴 Lecture 3

- Monotonic Stack Concept
- Next Greater Element
- Valid Parentheses
- Stock Span
- Daily Temperatures
- Interview Questions
- LeetCode Problems

---

# 📖 Key Takeaways

✅ Stack follows **LIFO (Last In, First Out)**.

✅ All insertion and deletion happen only at the **Top**.

✅ Basic operations (`push`, `pop`, `peek`) are **O(1)**.

✅ Stack is one of the most important data structures for:

- Recursion
- DFS
- Expression Evaluation
- Parentheses Matching
- Monotonic Stack Problems
- Browser History
- Undo / Redo