# 11. SORTING

## Definition

Sorting is the process of arranging elements in a particular order.

The two most common orders are:

- **Ascending Order** (Smallest to Largest)
- **Descending Order** (Largest to Smallest)

Example

Ascending

```
Input

5 2 8 1 4

Output

1 2 4 5 8
```

Descending

```
Input

5 2 8 1 4

Output

8 5 4 2 1
```

---

## Why Do We Need Sorting?

Sorting makes data easier to process and search.

Applications:

- Binary Search
- Finding Maximum/Minimum
- Finding Median
- Removing Duplicates
- Merging Arrays
- Pair Sum Problems

---

## Types of Sorting

There are many sorting algorithms.

We will study:

1. Bubble Sort
2. Selection Sort
3. Insertion Sort

---

# 1. Bubble Sort

## Idea

Bubble Sort compares **adjacent elements**.

If they are in the wrong order, they are swapped.

After every pass, the **largest element moves to its correct position**.

Example

```
5 1 4 2

Pass 1

1 4 2 5

Pass 2

1 2 4 5

Pass 3

1 2 4 5
```

### Algorithm

- Compare adjacent elements.
- Swap if left > right.
- Repeat for every pass.

### Time Complexity

- Best Case : O(n)
- Average Case : O(n²)
- Worst Case : O(n²)

---

# 2. Selection Sort

## Idea

Selection Sort repeatedly finds the **smallest element** from the unsorted part and places it at its correct position.

Example

```
5 3 1 4

Pass 1

1 3 5 4

Pass 2

1 3 5 4

Pass 3

1 3 4 5
```

### Algorithm

- Find the smallest element.
- Swap it with the current position.
- Repeat.

### Time Complexity

- Best Case : O(n²)
- Average Case : O(n²)
- Worst Case : O(n²)

---

# 3. Insertion Sort

## Idea

Insertion Sort assumes the left part is already sorted.

It picks one element and inserts it into the correct position.

Example

```
5 3 4 1

Pass 1

3 5 4 1

Pass 2

3 4 5 1

Pass 3

1 3 4 5
```

### Algorithm

- Pick one element.
- Compare it with previous elements.
- Insert it into the correct position.

### Time Complexity

- Best Case : O(n)
- Average Case : O(n²)
- Worst Case : O(n²)

---

# Comparison

| Algorithm | Best | Average | Worst | Stable |
|-----------|------|---------|--------|--------|
| Bubble Sort | O(n) | O(n²) | O(n²) | Yes |
| Selection Sort | O(n²) | O(n²) | O(n²) | No |
| Insertion Sort | O(n) | O(n²) | O(n²) | Yes |

---

# Practice Questions

## Question 1

Sort an array in ascending order using **Bubble Sort**.

---

## Question 2

Sort an array in descending order using **Bubble Sort**.

---

## Question 3

Sort an array in ascending order using **Selection Sort**.

---

## Question 4

Sort an array in ascending order using **Insertion Sort**.

---

## Question 5

Print the array after every pass of Bubble Sort.

---

## Question 6

Count the total number of swaps performed in Bubble Sort.

---

## Question 7

Find the second largest element by first sorting the array.

---

## Question 8

Check whether an array is already sorted.