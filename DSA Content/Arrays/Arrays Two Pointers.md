# 10. TWO POINTERS

## Definition

The **Two Pointer Technique** is an algorithmic approach where we use **two indices (pointers)** to solve a problem efficiently.

Instead of using only one index to traverse the array, we use **two pointers** that move according to the problem.

It helps reduce the time complexity of many problems from **O(n²)** to **O(n)**.

---

## When do we use Two Pointers?

- Reversing an array
- Checking if an array/string is a palindrome
- Finding pairs with a given sum (sorted array)
- Removing duplicates from a sorted array
- Moving zeros to the end
- Segregating even/odd or positive/negative numbers
- Merging sorted arrays

---

## Types of Two Pointer Problems

### 1. Opposite Direction

One pointer starts from the beginning and the other from the end.

```
Array

10 20 30 40 50

L               R
```

Both pointers move towards each other.

Used in:

- Reverse Array
- Palindrome Check
- Pair Sum (Sorted)

---

### 2. Same Direction

Both pointers start from the beginning.

```
0 1 2 3 4 5

L
R
```

The pointers move forward based on the condition.

Used in:

- Move Zeros
- Remove Duplicates
- Sliding Window (later)

---

## Basic Template (Opposite Direction)

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

## Basic Template (Same Direction)

```java
int left = 0;

for(int right = 0; right < arr.length; right++){

    // Process current element
}
```

---

# Two Pointer Practice Questions

---

## Level 1 : Basics

### Question 1

Reverse an array.

Example

```
Input

10 20 30 40 50

Output

50 40 30 20 10
```

---

### Question 2

Reverse only the first half of the array.

Example

```
Input

10 20 30 40 50 60

Output

30 20 10 40 50 60
```

---

### Question 3

Reverse only the second half of the array.

Example

```
Input

10 20 30 40 50 60

Output

10 20 30 60 50 40
```

---

### Question 4

Swap the first and last element.

Example

```
Input

10 20 30 40 50

Output

50 20 30 40 10
```

---

### Question 5

Swap every pair of adjacent elements.

Example

```
Input

1 2 3 4 5 6

Output

2 1 4 3 6 5
```

---

# Level 2 : Easy Logic

### Question 6

Check whether the array is a palindrome.

Example

```
Input

1 2 3 2 1

Output

Palindrome
```

---

### Question 7

Count the number of matching pairs from both ends.

Example

```
Input

1 2 3 2 1

Output

2
```

---

### Question 8

Move all zeros to the end.

Example

```
Input

1 0 3 0 5 0 2

Output

1 3 5 2 0 0 0
```

---

### Question 9

Move all zeros to the beginning.

Example

```
Input

1 0 3 0 5 0 2

Output

0 0 0 1 3 5 2
```

---

### Question 10

Move all negative numbers to the beginning.

Example

```
Input

2 -3 5 -1 8 -6

Output

-3 -1 -6 2 5 8
```

---

### Question 11

Move all positive numbers to the beginning.

Example

```
Input

2 -3 5 -1 8 -6

Output

2 5 8 -3 -1 -6
```

---

### Question 12

Separate even and odd numbers.

(Even numbers should come before odd numbers.)

Example

```
Input

3 2 7 8 5 4

Output

2 8 4 3 7 5
```

---

# Level 3 : Sorted Arrays

### Question 13

Find two numbers whose sum equals the target.

(Array is sorted.)

Example

```
Input

1 2 3 4 5 6

Target = 7

Output

1 6
```

---

### Question 14

Count the number of pairs having a given sum.

Example

```
Input

1 2 3 4 5 6

Target = 7

Output

3
```

---

### Question 15

Find all pairs having the given sum.

Example

```
Input

1 2 3 4 5 6

Target = 7

Output

1 6

2 5

3 4
```

---

# Level 4 : Good Problems

### Question 16

Remove duplicates from a sorted array.

Example

```
Input

1 1 2 2 3 3 4

Output

1 2 3 4
```

---

### Question 17

Merge two sorted arrays.

Example

```
Input

1 3 5

2 4 6

Output

1 2 3 4 5 6
```

---

### Question 18

Squares of a sorted array.

Example

```
Input

-4 -2 0 3 5

Output

0 4 9 16 25
```

---

### Question 19

Container With Most Water (Introduction)

---

### Question 20

Trapping Rain Water (Using Two Pointers)

---

# Important Observations

- If the problem involves **reversing**, think of **two pointers from opposite ends**.
- If the problem asks to **move elements** (zeros, negatives, etc.), think of **two pointers moving in the same direction**.
- If the array is **sorted** and asks for a **pair**, two pointers are often better than nested loops.
- Many interview problems can be optimized using the Two Pointer technique.