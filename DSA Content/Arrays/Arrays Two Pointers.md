> [!abstract] # 🎯 10. TWO POINTERS

---

> [!info] ## Definition

The **Two Pointer Technique** is an algorithmic approach where we use **two indices (pointers)** to solve a problem efficiently.

Instead of using only one index to traverse the array, we use **two pointers** that move according to the problem.

It helps reduce the time complexity of many problems from **O(n²)** to **O(n)**.

---

> [!tip] ## When do we use Two Pointers?

- ✅ Reversing an array
- ✅ Checking if an array/string is a palindrome
- ✅ Finding pairs with a given sum (sorted array)
- ✅ Removing duplicates from a sorted array
- ✅ Moving zeros to the end
- ✅ Segregating even/odd or positive/negative numbers
- ✅ Merging sorted arrays

---

> [!info] ## Types of Two Pointer Problems

### ① Opposite Direction

One pointer starts from the beginning and the other from the end.

```text
Array

10 20 30 40 50

L               R
```

Both pointers move towards each other.

**Used in:**

- Reverse Array
- Palindrome Check
- Pair Sum (Sorted)

---

### ② Same Direction

Both pointers start from the beginning.

```text
0 1 2 3 4 5

L
R
```

The pointers move forward based on the condition.

**Used in:**

- Move Zeros
- Remove Duplicates
- Sliding Window (later)

---

> [!example] ## Basic Template (Opposite Direction)

```java
int left = 0;
int right = arr.length - 1;

while(left < right){

    // Perform required operation

    left++;
    right--;
}
```

---

> [!example] ## Basic Template (Same Direction)

```java
int left = 0;

for(int right = 0; right < arr.length; right++){

    // Process current element
}
```

---

> [!question] # Two Pointer Practice Questions

---

## 🟢 Level 1 : Basics

---

> [!question] ### Question 1

Reverse an array.

### Example

```text
Input

10 20 30 40 50

Output

50 40 30 20 10
```

---

> [!question] ### Question 2

Reverse only the first half of the array.

### Example

```text
Input

10 20 30 40 50 60

Output

30 20 10 40 50 60
```

---

> [!question] ### Question 3

Reverse only the second half of the array.

### Example

```text
Input

10 20 30 40 50 60

Output

10 20 30 60 50 40
```

---

> [!question] ### Question 4

Swap the first and last element.

### Example

```text
Input

10 20 30 40 50

Output

50 20 30 40 10
```

---

> [!question] ### Question 5

Swap every pair of adjacent elements.

### Example

```text
Input

1 2 3 4 5 6

Output

2 1 4 3 6 5
```

---

## 🟡 Level 2 : Easy Logic

---

> [!question] ### Question 6

Check whether the array is a palindrome.

### Example

```text
Input

1 2 3 2 1

Output

Palindrome
```

---

> [!question] ### Question 7

Count the number of matching pairs from both ends.

### Example

```text
Input

1 2 3 2 1

Output

2
```

---

> [!question] ### Question 8

Move all zeros to the end.

### Example

```text
Input

1 0 3 0 5 0 2

Output

1 3 5 2 0 0 0
```

---

> [!question] ### Question 9

Move all zeros to the beginning.

### Example

```text
Input

1 0 3 0 5 0 2

Output

0 0 0 1 3 5 2
```

---

> [!question] ### Question 10

Move all negative numbers to the beginning.

### Example

```text
Input

2 -3 5 -1 8 -6

Output

-3 -1 -6 2 5 8
```

---

> [!question] ### Question 11

Move all positive numbers to the beginning.

### Example

```text
Input

2 -3 5 -1 8 -6

Output

2 5 8 -3 -1 -6
```

---

> [!question] ### Question 12

Separate even and odd numbers.

(Even numbers should come before odd numbers.)

### Example

```text
Input

3 2 7 8 5 4

Output

2 8 4 3 7 5
```

---

## 🟠 Level 3 : Sorted Arrays

---

> [!question] ### Question 13

Find two numbers whose sum equals the target.

(Array is sorted.)

### Example

```text
Input

1 2 3 4 5 6

Target = 7

Output

1 6
```

---

> [!question] ### Question 14

Count the number of pairs having a given sum.

### Example

```text
Input

1 2 3 4 5 6

Target = 7

Output

3
```

---

> [!question] ### Question 15

Find all pairs having the given sum.

### Example

```text
Input

1 2 3 4 5 6

Target = 7

Output

1 6

2 5

3 4
```

---

## 🔴 Level 4 : Good Problems

---

> [!question] ### Question 16

Remove duplicates from a sorted array.

### Example

```text
Input

1 1 2 2 3 3 4

Output

1 2 3 4
```

---

> [!question] ### Question 17

Merge two sorted arrays.

### Example

```text
Input

1 3 5

2 4 6

Output

1 2 3 4 5 6
```

---

> [!question] ### Question 18

Squares of a sorted array.

### Example

```text
Input

-4 -2 0 3 5

Output

0 4 9 16 25
```

---

> [!question] ### Question 19

Container With Most Water (Introduction)

---

> [!question] ### Question 20

Trapping Rain Water (Using Two Pointers)

---

> [!important] ## 📌 Important Observations

- 📍 If the problem involves **reversing**, think of **two pointers from opposite ends**.
- 📍 If the problem asks to **move elements** (zeros, negatives, etc.), think of **two pointers moving in the same direction**.
- 📍 If the array is **sorted** and asks for a **pair**, two pointers are often better than nested loops.
- 📍 Many interview problems can be optimized using the **Two Pointer Technique**.

---

> [!success] 🎯 Key Takeaway

Before solving any array problem, ask yourself:

- ❓ Can I solve this using **two pointers** instead of nested loops?
- ❓ Can I reduce the complexity from **O(n²)** to **O(n)**?

If the answer is **Yes**, the Two Pointer Technique is probably the right approach.