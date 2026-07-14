# 9. ARRAYS

## Definition

An array is a collection of elements of the **same data type** stored in **contiguous memory locations**.

Instead of creating multiple variables, we can store all values in a single array.

### Without Array

```java
int a = 10;
int b = 20;
int c = 30;
int d = 40;
int e = 50;
```

### With Array

```java
int[] arr = {10, 20, 30, 40, 50};
```

---

## Why Arrays?

- Store multiple values using one variable.
- Easy to traverse using loops.
- Less code.
- Better organization of data.

---

## Array Index

Every element has an index.

**Index always starts from 0.**

```
Index :   0   1   2   3   4
Value :  10  20  30  40  50
```

Example:

```java
int[] arr = {10,20,30,40,50};

System.out.println(arr[0]); // 10
System.out.println(arr[2]); // 30
System.out.println(arr[4]); // 50
```

---

## Declaring an Array

```java
int[] arr;
```

---

## Creating an Array

```java
int[] arr = new int[5];
```

Initially,

```
Index : 0 1 2 3 4
Value : 0 0 0 0 0
```

---

## Declaration + Initialization

```java
int[] arr = {10,20,30,40,50};
```

---

## Assigning Values

```java
int[] arr = new int[5];

arr[0] = 10;
arr[1] = 20;
arr[2] = 30;
arr[3] = 40;
arr[4] = 50;
```

---

## Printing Elements

```java
int[] arr = {10,20,30,40,50};

System.out.println(arr[0]);
System.out.println(arr[1]);
System.out.println(arr[2]);
```

---

## Printing Using Loop

```java
int[] arr = {10,20,30,40,50};

for(int i=0;i<5;i++){
    System.out.println(arr[i]);
}
```

Better way:

```java
for(int i=0;i<arr.length;i++){
    System.out.println(arr[i]);
}
```

---

## length Property

```java
int[] arr = {10,20,30,40,50};

System.out.println(arr.length);
```

Output

```
5
```

---

## Taking Input

```java
Scanner sc = new Scanner(System.in);

int[] arr = new int[5];

for(int i=0;i<arr.length;i++){
    arr[i] = sc.nextInt();
}
```

---

## Printing User Input

```java
for(int i=0;i<arr.length;i++){
    System.out.print(arr[i] + " ");
}
```

---

