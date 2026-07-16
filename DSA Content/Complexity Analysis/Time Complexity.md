> [!abstract] ## 🚀 Why Optimization Matters
> Optimization means making a program **faster** and/or using **less memory**.
>
> The same problem can have multiple solutions, but some are much more efficient than others.

> [!example]
> **Example: Find the maximum element in an array**
>
> **Method 1:** Sort the array and return the last element.
>
> **Method 2:** Traverse the array once and keep track of the maximum.
>
> ✅ Method 2 is better because it does less work.

---

# ⏱️ Time Complexity

> [!info]
> Time Complexity measures **how the running time of an algorithm grows as the input size increases**.
>
> It does **not** measure actual time in seconds because different computers have different speeds.
>
> Instead, it measures the **number of operations** performed.
>
> **Big-O notation** is used to represent time complexity.

---

# 📊 Common Time Complexities

> [!tip] ## 🟢 1. Constant Time – O(1)

- Number of operations remains the same regardless of input size.
- Fastest time complexity.

### Examples

- Accessing an array element by index
- Stack Push/Pop
- Queue Enqueue/Dequeue

```java
int x = arr[5];
```

---

> [!tip] ## 🔵 2. Linear Time – O(n)

- Operations increase directly with the input size.
- Every element is processed once.

### Examples

- Linear Search
- Finding Maximum/Minimum
- Sum of Array
- Printing Array

```java
for(int i=0;i<n;i++){
    System.out.println(arr[i]);
}
```

---

> [!tip] ## 🟡 3. Quadratic Time – O(n²)

- Usually caused by two nested loops.
- Every element is compared with every other element.

### Examples

- Bubble Sort
- Selection Sort
- Printing all pairs

```java
for(int i=0;i<n;i++){
    for(int j=0;j<n;j++){
        // work
    }
}
```

---

> [!tip] ## 🟠 4. Cubic Time – O(n³)

- Three nested loops.
- Becomes very slow for large inputs.

### Examples

- Printing all triplets
- Brute-force 3Sum
- Floyd Warshall Algorithm

```java
for(int i=0;i<n;i++){
    for(int j=0;j<n;j++){
        for(int k=0;k<n;k++){
            // work
        }
    }
}
```

---

> [!success] ## 🟢 5. Logarithmic Time – O(log n)

- Input size is reduced by half in each step.
- Extremely efficient for large inputs.

### Examples

- Binary Search

```java
while(left <= right){
    int mid = (left + right) / 2;
}
```

Example

```text
1024
↓
512
↓
256
↓
...
↓
1
```

Only about **10 steps**.

---

> [!success] ## 🔷 6. Linearithmic Time – O(n log n)

- Combination of Linear and Logarithmic.
- Used by efficient sorting algorithms.

### Examples

- Merge Sort
- Heap Sort
- Quick Sort (Average Case)

---

> [!warning] ## 🔴 7. Exponential Time – O(2ⁿ)

- Work doubles whenever input increases by one.
- Extremely slow for large inputs.

### Examples

- Generating all subsets
- Naive Fibonacci
- Backtracking

```text
n = 3 → 8
n = 4 → 16
n = 5 → 32
n = 20 → 1,048,576
```

---

> [!example] ## 📈 Complexity Order (Best to Worst)

```text
🟢 O(1)
      ↓
🟢 O(log n)
      ↓
🔵 O(n)
      ↓
🟡 O(n log n)
      ↓
🟠 O(n²)
      ↓
🔴 O(n³)
      ↓
⛔ O(2ⁿ)
```

---

> [!summary] ## 📋 Summary Table

| Complexity | Name | Common Examples |
|------------|------|-----------------|
| 🟢 O(1) | Constant | Array Access, Stack Operations |
| 🟢 O(log n) | Logarithmic | Binary Search |
| 🔵 O(n) | Linear | Linear Search, Sum of Array |
| 🟡 O(n log n) | Linearithmic | Merge Sort, Heap Sort |
| 🟠 O(n²) | Quadratic | Bubble Sort, Selection Sort |
| 🔴 O(n³) | Cubic | Floyd Warshall, Triplets |
| ⛔ O(2ⁿ) | Exponential | Subsets, Naive Fibonacci |

---

> [!important] ## ⭐ Key Points

- Choose algorithms that perform fewer operations.
- Time complexity focuses on **growth with input size**, not actual execution time.
- **O(1), O(log n), O(n), and O(n log n)** are generally considered efficient.
- **O(n²)** is acceptable for small inputs.
- **O(n³)** and **O(2ⁿ)** should be avoided for large inputs whenever possible.

---

# 💪 Brute Force

> [!info]
> A **Brute Force** approach is the simplest and most straightforward way to solve a problem.
>
> It usually checks **all possible cases** without trying to optimize.

### Characteristics

- ✅ Easy to understand and implement.
- ❌ Usually slower for large inputs.
- 💡 Good as the first solution.

### Examples

- Linear Search
- Bubble Sort
- Checking every pair in an array

---

# ⚡ Optimized Approach

> [!success]
> An **Optimized** approach solves the same problem using **fewer operations**, making the program faster and more efficient.

### Characteristics

- Uses better algorithms or data structures.
- Reduces time and/or space complexity.
- Preferred for large inputs.

### Examples

- Binary Search instead of Linear Search.
- HashMap instead of nested loops.
- Merge Sort instead of Bubble Sort.

---

# 🟢 Best Case

> [!tip]
> The **Best Case** is the minimum time an algorithm takes for the most favorable input.

### Example

Linear Search

```java
int[] arr = {10,20,30,40};
target = 10;
```

Target is found in the **first comparison**.

**Time Complexity:** **O(1)**

---

# 🔴 Worst Case

> [!warning]
> The **Worst Case** is the maximum time an algorithm takes for the least favorable input.

### Example

Linear Search

```java
int[] arr = {10,20,30,40};
target = 40;
```

or

```java
target = 100;
```

Need to check every element.

**Time Complexity:** **O(n)**

---

# 🟡 Average Case

> [!info]
> The **Average Case** is the expected running time for a random input.

It lies between the best and worst cases.

### Example

Linear Search

If the target is equally likely to be anywhere in the array, on average about **n/2 elements** are checked.

**Time Complexity:** **O(n)**

---

# 💾 Space Complexity

> [!abstract]
> **Space Complexity** measures the amount of **extra memory** used by an algorithm during execution.

It includes:

- Variables
- Temporary arrays
- Stack space (recursion)

---

> [!example] ### 🟢 O(1) Space

Only a few variables are used.

```java
int sum = 0;
for(int i=0;i<n;i++){
    sum += arr[i];
}
```

Extra space remains constant.

---

> [!example] ### 🔵 O(n) Space

Extra array is created.

```java
int[] temp = new int[n];
```

Memory increases with input size.

---

> [!example] ### 🟢 O(log n) Space

Used by recursive algorithms like Binary Search.

Recursive call stack grows logarithmically.

---

# ⚖️ Time vs Space Trade-off

> [!tip]
> Sometimes we use **more memory to reduce execution time**.

### Example

Finding duplicate elements

**Method 1**

- Nested loops
- Time: **O(n²)**
- Space: **O(1)**

**Method 2**

- HashSet
- Time: **O(n)**
- Space: **O(n)**

This is called a **Time-Space Trade-off**.

---

> [!summary] ## 📚 Summary

| Term | Meaning |
|------|---------|
| 💪 Brute Force | Simple solution that checks all possibilities |
| ⚡ Optimized | Faster and more efficient solution |
| 📈 Big-O | Describes how running time grows with input size |
| 🟢 Best Case | Minimum running time |
| 🟡 Average Case | Expected running time for random input |
| 🔴 Worst Case | Maximum running time |
| 💾 Space Complexity | Extra memory used by an algorithm |

---

> [!important] ## 🎯 Key Points

- Start with a **Brute Force** solution, then optimize it.
- Big-O focuses on **growth**, not actual execution time.
- Worst-case complexity is the most commonly used for comparing algorithms.
- An efficient algorithm should aim for **low time complexity** and **low space complexity**, while balancing the **time-space trade-off** when necessary.