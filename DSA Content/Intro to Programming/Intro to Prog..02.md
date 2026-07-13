  # 7. NESTED LOOPS

A nested loop is a loop inside another loop.

Rule:

One row = One iteration of the outer loop.

==================================================================

Outer Loop

    ↓

How many rows?

-------------------------

Inner Loop

    ↓

How many columns?

==================================================================

## Example 1

```java

for(int i = 1; i <= 3; i++){

   for(int j = 1; j <= 5; j++){

   System.out.print("*");

  }

System.out.println();

}

```

Output

---

---

---

==================================================================

## Example 2

```java

for(int i = 1; i <= 3; i++){

    for(int j = 1; j <= 5; j++){

        System.out.print(j);

    }

    System.out.println();

}

```

Output

12345

12345

12345

==================================================================

## Example 3

```java

for(int i = 1; i <= 3; i++){

    for(int j = 1; j <= 5; j++){

        System.out.print(i);

    }

    System.out.println();

}

```

Output

11111

22222

33333

==================================================================

## Example 4

```java

for(int i = 1; i <= 2; i++){

    for(int j = 1; j <= 3; j++){

        System.out.print("*");

    }

    System.out.println();

}

```

Output

---

---

==================================================================

## Example 5

```java

for(int i = 1; i <= 3; i++){

    for(int j = 1; j <= 2; j++){

        System.out.print(i);

    }

    System.out.println();

}

```

Output

11

22

33

==================================================================

## Example 6

```java

for(int i = 1; i <= 4; i++){

    for(int j = 1; j <= 4; j++){

        System.out.print(i + j);

    }

    System.out.println();

}

```

Output

2345

3456

4567

5678

==================================================================

# 8. PATTERN PRINTING

Print the following patterns using nested loops.

==================================================================

### Pattern 1

###

###

###

###

==================================================================

### Pattern 2

12345

23456

34567

45678

56789

==================================================================

### Pattern 3

2 4 6 8 10

2 4 6 8 10

2 4 6 8 10

2 4 6 8 10

2 4 6 8 10

==================================================================

### Pattern 4

**

---

---

---

==================================================================

### Pattern 5

---

---

---

**

==================================================================

### Pattern 6

1

12

123

1234

12345

==================================================================

### Pattern 7

1

22

333

4444

55555

==================================================================

### Pattern 8

54321

5432

543

54

5

==================================================================

### Pattern 9

12345

1234

123

12

1

==================================================================

### Pattern 10

54321

5432

543

54

5

==================================================================

### Pattern 11

5

54

543

5432

54321

==================================================================

### Pattern 12

5

45

345

2345

12345

==================================================================

### Pattern 13

11111

2222

333

44

5

==================================================================

### Pattern 14

12321

12321

12321

12321

12321

==================================================================

### Pattern 15 (Floyd's Triangle)

Output

1

2 3

4 5 6

7 8 9 10

11 12 13 14 15

int num = 1;

for(int i = 1; i <= 5; i++){

for(int j = 1; j <= i; j++){

System.out.print(num++ + " ");

}

System.out.println();

}





### #FUNCTIONS



Definition:

A function (or method) is a block of code that performs a specific task.

Example:

Think of a TV remote.

- Press Power -> TV turns on.

- Press Volume Up -> Volume increases.

- Press Channel Down -> Channel changes.

General Syntax:

returnType methodName(parameters) {

    // code

}

Examples:

1. int sum(int a, int b) {

       return a + b;

   }

2. void greet() {

       System.out.println("Good Morning");

   }

Practice Questions:

3. Create a method to find the square of a number.

4. Create a method to return the larger of two numbers.

5. Create a method to check whether a number is even or odd.