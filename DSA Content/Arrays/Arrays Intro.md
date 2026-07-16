> [!abstract] # 📦 9. ARRAYS

---

> [!info] ## Definition

An array is a collection of elements of the **same data type** stored in **contiguous memory locations**.

Instead of creating multiple variables, we can store all values in a single array.

---

## 📝 Without Array

```java
int a = 10;
int b = 20;
int c = 30;
int d = 40;
int e = 50;
```

---

## 📝 With Array

```java
int[] arr = {10, 20, 30, 40, 50};
```

---

> [!tip] ## Why Arrays?

- ✅ Store multiple values using one variable.
- ✅ Easy to traverse using loops.
- ✅ Less code.
- ✅ Better organization of data.

---

> [!info] ## Array Index

Every element has an index.

**Index always starts from 0.**

```text
Index :   0   1   2   3   4
Value :  10  20  30  40  50
```

### Example

```java
int[] arr = {10,20,30,40,50};

System.out.println(arr[0]); // 10
System.out.println(arr[2]); // 30
System.out.println(arr[4]); // 50
```

---

> [!success] ## Declaring an Array

```java
int[] arr;
```

---

> [!success] ## Creating an Array

```java
int[] arr = new int[5];
```

Initially,

```text
Index : 0 1 2 3 4
Value : 0 0 0 0 0
```

---

> [!success] ## Declaration + Initialization

```java
int[] arr = {10,20,30,40,50};
```

---

> [!success] ## Assigning Values

```java
int[] arr = new int[5];

arr[0] = 10;
arr[1] = 20;
arr[2] = 30;
arr[3] = 40;
arr[4] = 50;
```

---

> [!example] ## Printing Elements

```java
int[] arr = {10,20,30,40,50};

System.out.println(arr[0]);
System.out.println(arr[1]);
System.out.println(arr[2]);
```

---

> [!example] ## Printing Using Loop

```java
int[] arr = {10,20,30,40,50};

for(int i=0;i<5;i++){
    System.out.println(arr[i]);
}
```

### 💡 Better Way

```java
for(int i=0;i<arr.length;i++){
    System.out.println(arr[i]);
}
```

---

> [!tip] ## `length` Property

```java
int[] arr = {10,20,30,40,50};

System.out.println(arr.length);
```

### ✅ Output

```text
5
```

---

> [!example] ## Taking Input

```java
Scanner sc = new Scanner(System.in);

int[] arr = new int[5];

for(int i=0;i<arr.length;i++){
    arr[i] = sc.nextInt();
}
```

---

> [!example] ## Printing User Input

```java
for(int i=0;i<arr.length;i++){
    System.out.print(arr[i] + " ");
}
```

---

> [!important] ## 📌 Key Points

- 📍 Arrays store elements of the **same data type**.
- 📍 Array indexing always starts from **0**.
- 📍 Elements are stored in **contiguous memory locations**.
- 📍 Use **`arr.length`** instead of hardcoding the array size.
- 📍 Arrays have a **fixed size** once created.
- 📍 Loops are the easiest way to traverse an array.