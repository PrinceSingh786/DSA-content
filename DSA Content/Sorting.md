> [!abstract] # 11. 🔄 SORTING

Sorting is the process of arranging elements in a particular order.

There are two common orders:

- 🟢 **Ascending Order** (Smallest → Largest)
- 🔴 **Descending Order** (Largest → Smallest)

### Example

**Ascending**

```text
Input

5 2 8 1 4

Output

1 2 4 5 8
```

**Descending**

```text
Input

5 2 8 1 4

Output

8 5 4 2 1
```

---

> [!info] ## Why Do We Need Sorting?

Sorting makes data easier to process and search.

### Applications

- 🔍 Binary Search
- 📈 Finding Maximum / Minimum
- 📊 Finding Median
- ❌ Removing Duplicates
- 🔀 Merging Arrays
- 🎯 Pair Sum Problems

---

> [!tip] ## Types of Sorting

We will study the following sorting algorithms:

1. 🫧 Bubble Sort
2. 🎯 Selection Sort
3. 📥 Insertion Sort

---

# 🫧 1. Bubble Sort

> [!info] ## Idea

Bubble Sort compares **adjacent elements**.

If they are in the wrong order, they are swapped.

After every pass, the **largest element reaches its correct position**.

### Example

```text
5 1 4 2

Pass 1

1 4 2 5

Pass 2

1 2 4 5

Pass 3

1 2 4 5
```

---

### Algorithm

- Compare adjacent elements.
- Swap if the left element is greater than the right element.
- Repeat for every pass.

---

> [!success] ### Time Complexity

| Case | Complexity |
|------|------------|
| 🟢 Best | **O(n)** |
| 🟡 Average | **O(n²)** |
| 🔴 Worst | **O(n²)** |

---

# 🎯 2. Selection Sort

> [!info] ## Idea

Selection Sort repeatedly finds the **smallest element** from the unsorted part and places it at its correct position.

### Example

```text
5 3 1 4

Pass 1

1 3 5 4

Pass 2

1 3 5 4

Pass 3

1 3 4 5
```

---

### Algorithm

- Find the smallest element.
- Swap it with the current position.
- Repeat until the array is sorted.

---

> [!success] ### Time Complexity

| Case | Complexity |
|------|------------|
| 🟢 Best | **O(n²)** |
| 🟡 Average | **O(n²)** |
| 🔴 Worst | **O(n²)** |

---

# 📥 3. Insertion Sort

> [!info] ## Idea

Insertion Sort assumes the left part of the array is already sorted.

It picks one element and inserts it into its correct position.

### Example

```text
5 3 4 1

Pass 1

3 5 4 1

Pass 2

3 4 5 1

Pass 3

1 3 4 5
```

---

### Algorithm

- Pick one element.
- Compare it with previous elements.
- Insert it into its correct position.

---

> [!success] ### Time Complexity

| Case | Complexity |
|------|------------|
| 🟢 Best | **O(n)** |
| 🟡 Average | **O(n²)** |
| 🔴 Worst | **O(n²)** |

---

> [!example] # Comparison

| Algorithm | Best | Average | Worst | Stable |
|-----------|------|---------|--------|--------|
| 🫧 Bubble Sort | **O(n)** | **O(n²)** | **O(n²)** | ✅ Yes |
| 🎯 Selection Sort | **O(n²)** | **O(n²)** | **O(n²)** | ❌ No |
| 📥 Insertion Sort | **O(n)** | **O(n²)** | **O(n²)** | ✅ Yes |

---

> [!question] # Practice Questions

### Question 1

Sort an array in **ascending order** using **Bubble Sort**.

---

### Question 2

Sort an array in **descending order** using **Bubble Sort**.

---

### Question 3

Sort an array in **ascending order** using **Selection Sort**.

---

### Question 4

Sort an array in **ascending order** using **Insertion Sort**.

---

### Question 5

Print the array after every pass of **Bubble Sort**.

---

### Question 6

Count the total number of **swaps** performed in Bubble Sort.

---

### Question 7

Find the **second largest element** by first sorting the array.

---

### Question 8

Check whether an array is **already sorted**.