# **Intro to Programming**











### **# 1. VARIABLES**



Definition:

A variable is a named memory location (memory block) used to store data.



Example:

int age = 20;



==================================================================











### **# 2. DATA TYPES**



&#x20;                   Data Types

&#x20;                       │

&#x20;         ┌─────────────┴─────────────┐

&#x20;         │                           │

&#x20;    Primitive                 Non-Primitive

&#x20;                                (Reference)



Primitive Data Types

\--------------------

• byte

• short

• int      (4 bytes)

• long     (8 bytes)

• float    (4 bytes)

• double   (8 bytes)

• char

• Boolean

















## **# 3. OPERATORS**



Operators are special symbols used to perform operations on variables and values.



==================================================================



**## 1. Arithmetic Operators**



Used for mathematical calculations.



\------------------------------------------------------------

| Operator | Meaning                 | Example             |

\------------------------------------------------------------

| +        | Addition                | a + b               |

| -        | Subtraction             | a - b               |

| \*        | Multiplication          | a \* b               |

| /        | Division                | a / b               |

| %        | Modulus (Remainder)     | a % b               |

\------------------------------------------------------------



Example:



```java

int a = 10;

int b = 3;



System.out.println(a + b);   // 13

System.out.println(a - b);   // 7

System.out.println(a \\\\\\\* b);   // 30

System.out.println(a / b);   // 3

System.out.println(a % b);   // 1

```



Important:

Integer division discards the decimal part.



```java

System.out.println(7 / 2);     // 3

System.out.println(7.0 / 2);   // 3.5

```



==================================================================



**## 2. Assignment Operators**



Used to assign values to variables.



Example:



```java

int x = 10;

```



Compound Assignment Operators



\--------------------------------------------------

| Operator | Meaning                             |

\--------------------------------------------------

| +=       | x = x + y                           |

| -=       | x = x - y                           |

| \*=       | x = x \* y                           |

| /=       | x = x / y                           |

| %=       | x = x % y                           |

\--------------------------------------------------



Example:



```java

int x = 10;



x += 5;

System.out.println(x);     // 15



x \\\\\\\*= 2;

System.out.println(x);     // 30

```



==================================================================



**## 3. Relational Operators**



Used to compare two values.

The result is always true or false.



\-------------------------------------------------------

| Operator | Meaning                                 |

\-------------------------------------------------------

| ==       | Equal to                                |

| !=       | Not Equal to                            |

| >        | Greater than                            |

| <        | Less than                               |

| >=       | Greater than or Equal to                |

| <=       | Less than or Equal to                   |

\-------------------------------------------------------



Example:



```java

int a = 10;

int b = 20;



System.out.println(a == b);   // false

System.out.println(a != b);   // true

System.out.println(a < b);    // true

```



==================================================================



**## 4. Logical Operators**



Used with boolean expressions.



\------------------------------------------------------

| Operator | Meaning                                |

\------------------------------------------------------

| \&\&       | Logical AND                            |

| ||       | Logical OR                             |

| !        | Logical NOT                            |

\------------------------------------------------------



Example:



```java

int age = 20;

boolean hasID = true;



System.out.println(age >= 18 \\\\\\\&\\\\\\\& hasID);   // true

System.out.println(age < 18 || hasID);    // true

System.out.println(!hasID);               // false

```



Short-Circuit Evaluation



• \&\& stops if the left side is false.



• || stops if the left side is true.



==================================================================



**## 5. Unary Operators**



Operate on a single operand.



Example:



```java

int x = 5;



System.out.println(+x);   // 5

System.out.println(-x);   // -5

```



==================================================================



**## 6. Increment and Decrement Operators**



Used to increase or decrease a value by 1.



Example:



```java

int x = 5;



x++;

System.out.println(x);   // 6



x--;

System.out.println(x);   // 5

```



\### Pre vs Post Increment



```java

int a = 5;



System.out.println(++a);   // 6



int b = 5;



System.out.println(b++);   // 5

System.out.println(b);     // 6

```



Similarly,



```java

\\\\--a;

a--;

```



==================================================================



**## 7. Ternary Operator**



A shorthand for if-else.



Syntax:



```java

condition ? value\\\\\\\_if\\\\\\\_true : value\\\\\\\_if\\\\\\\_false;

```



Example:



```java

int age = 20;



String result = (age >= 18) ? "Adult" : "Minor";



System.out.println(result);

```



==================================================================



**## Operator Precedence (Highest to Lowest)**



1\. ()            → Parentheses

2\. Unary         → ++, --, !, +, -

3\. \*, /, %

4\. +, -

5\. Relational    → <, >, <=, >=

6\. Equality      → ==, !=

7\. \&\&

8\. ||

9\. Assignment    → =, +=, -=, \*=, /=, %=



==================================================================







## **# 4. INPUT / OUTPUT**



Practice Question:

Take your PRN Number as input and print it.



Example:



```java

import java.util.Scanner;



Scanner sc = new Scanner(System.in);



System.out.print("Enter PRN Number: ");

String prn = sc.nextLine();



System.out.println("PRN Number: " + prn);

```



==================================================================



# **# 5. IF - ELSE**



The if-else statement is used to make decisions based on a condition.



Flow of Problems



Voting Eligibility

&#x20;       │

&#x20;       ▼

Positive / Negative / Zero

&#x20;       │

&#x20;       ▼

Even or Odd

&#x20;       │

&#x20;       ▼

Largest of Two Numbers

&#x20;       │

&#x20;       ▼

Largest of Three Numbers

&#x20;       │

&#x20;       ▼

Leap Year

&#x20;       │

&#x20;       ▼

Grade Calculator

&#x20;       │

&#x20;       ▼

Electricity Bill

&#x20;       │

&#x20;       ▼

Income Tax Slab



==================================================================



\## Electricity Bill



```java

if(units <= 100){

&#x20;   bill = units \* 5;

}

else if(units <= 200){

&#x20;   bill = (100 \* 5) + ((units - 100) \* 7);

}

else{

&#x20;   bill = (100 \* 5) + (100 \* 7)

&#x20;        + ((units - 200) \* 10);

}

```



==================================================================



\## Income Tax Slab



```java

if(income <= 250000){

&#x20;   tax = 0;

}

else if(income <= 500000){

&#x20;   tax = income \* 0.05;

}

else if(income <= 1000000){

&#x20;   tax = income \* 0.20;

}

else{

&#x20;   tax = income \* 0.30;

}

```



==================================================================



#### **## Else-If Ladder**



```java

if(condition1){



}

else if(condition2){



}

else if(condition3){



}

else{



}

```



==================================================================



### **## Nested If**



```java

int age = 22;

boolean license = true;



if(age >= 18){



&#x20;   if(license){

&#x20;       System.out.println("Can Drive");

&#x20;   }

&#x20;   else{

&#x20;       System.out.println("Need License");

&#x20;   }



}

else{

&#x20;   System.out.println("Too Young");

}

```



==================================================================



### **#  SWITCH STATEMENT**



Syntax



```java

switch(expression){



&#x20;   case value1:

&#x20;       statements;

&#x20;       break;



&#x20;   case value2:

&#x20;       statements;

&#x20;       break;



&#x20;   default:

&#x20;       statements;

}

```



==================================================================



\## Example



```java

int day = 3;



switch(day){



&#x20;   case 1:

&#x20;       System.out.println("Monday");

&#x20;       break;



&#x20;   case 2:

&#x20;       System.out.println("Tuesday");

&#x20;       break;



&#x20;   case 3:

&#x20;       System.out.println("Wednesday");

&#x20;       break;



&#x20;   default:

&#x20;       System.out.println("Invalid");

}

```



==================================================================















## **# 6. LOOPS**



A loop is used to execute a block of code repeatedly until a given condition becomes false.



Example:

Print "Hello" 1000 times.



==================================================================



\## Types of Loops



1\. **for Loop**

**2. while Loop**

**3. do-while Loop**



==================================================================



##### **## 1. FOR LOOP**



\### Syntax



```java

for(initialization; condition; update){

\\\&#x20;   // body

}

```



\### Example



```java

for(int i = 1; i <= 4; i++){

\\\&#x20;   System.out.println(i);

}

```



\### More Examples



Print even numbers from 2 to 20



```java

for(int i = 2; i <= 20; i += 2){

\\\&#x20;   System.out.print(i + " ");

}

```



Print multiples of 5



```java

for(int i = 5; i <= 100; i += 5){

\\\&#x20;   System.out.print(i + " ");

}

```









==================================================================



##### **## Output Guessing Questions (for Loop)**



\### 1.



```java

for(int i = 1; i <= 5; i++){

\\\&#x20;   System.out.print(i + " ");

}

```



\### 2.



```java

for(int i = 5; i >= 1; i--){

\\\&#x20;   System.out.print(i + " ");

}

```



\### 3.



```java

for(int i = 2; i <= 10; i += 2){

\\\&#x20;   System.out.print(i + " ");

}

```



\### 4.



```java

for(int i = 1; i <= 10; i += 3){

\\\&#x20;   System.out.print(i + " ");

}

```



\### 5.



```java

for(int i = 10; i > 0; i -= 2){

\\\&#x20;   System.out.print(i + " ");

}

```



==================================================================



\## Practice Questions



1\. Print all even numbers from 1 to N.



2\. Print all numbers divisible by 5 from 1 to 30.



3\. Find the sum of numbers from 1 to 50.









==================================================================



##### **## 2. WHILE LOOP**



\### Syntax



```java

while(condition){

\\\&#x20;   // body

}

```



\### Example



```java

int i = 1;



while(i <= 4){

\\\&#x20;   System.out.println(i);

\\\&#x20;   i++;

}

```











==================================================================



##### **## Output Guessing Questions (while Loop)**



\### 1.



```java

int i = 1;



while(i <= 5){

\\\&#x20;   System.out.println(i);

\\\&#x20;   i++;

}

```



\### 2.



```java

int i = 2;



while(i <= 10){

\\\&#x20;   System.out.print(i + " ");

\\\&#x20;   i = i + 2;

}

```



\### 3.



```java

int i = 10;



while(i >= 1){

\\\&#x20;   System.out.print(i + " ");

\\\&#x20;   i--;

}

```



\### 4.



```java

int i = 1;



while(i <= 5){

\\\&#x20;   System.out.print(i \\\\\\\* i + " ");

\\\&#x20;   i++;

}

```



\### 5.



```java

int i = 1;



while(i <= 5){

\\\&#x20;   System.out.print(i + 2 + " ");

\\\&#x20;   i++;

}

```















==================================================================



##### **## 3. DO-WHILE LOOP**



\### Syntax



```java

do{

\\\&#x20;   // body

}

while(condition);

```



\### Example



```java

int i = 1;



do{

\\\&#x20;   System.out.println(i);

\\\&#x20;   i++;

}

while(i <= 4);

```















==================================================================



##### **## Output Guessing Questions (do-while Loop)**



\### 1.



```java

int i = 1;



do{

\\\&#x20;   System.out.println(i);

\\\&#x20;   i++;

}

while(i <= 5);

```



\### 2.



```java

int i = 10;



do{

\\\&#x20;   System.out.println(i);

\\\&#x20;   i++;

}

while(i <= 5);

```



\### 3.



```java

int i = 10;



do{

\\\&#x20;   System.out.print(i + " ");

\\\&#x20;   i -= 3;

}

while(i >= 1);

```



\### 4.



```java

int i = 3;



do{

\\\&#x20;   System.out.print(i \\\\\\\* 2 + " ");

\\\&#x20;   i++;

}

while(i <= 6);

```



\### 5.



```java

int i = 1;



do{

\\\&#x20;   System.out.print(i + " ");

\\\&#x20;   i++;

\\\&#x20;   i++;

}

while(i <= 7);

```



\### 6.



```java

int i = 2;



do{

\\\&#x20;   System.out.print(i \\\\\\\* i + " ");

\\\&#x20;   i += 2;

}

while(i <= 8);

```



==================================================================

















# **# 7. NESTED LOOPS**



A nested loop is a loop inside another loop.



Rule:

One row = One iteration of the outer loop.



==================================================================



Outer Loop

&#x20;   ↓

How many rows?



\-------------------------



Inner Loop

&#x20;   ↓

How many columns?



==================================================================



\## Example 1



```java

for(int i = 1; i <= 3; i++){



\\\&#x20;   for(int j = 1; j <= 5; j++){

\\\&#x20;       System.out.print("\\\\\\\*");

\\\&#x20;   }



\\\&#x20;   System.out.println();

}

```



Output



**\*\*\*\*\***

**\*\*\*\*\***

**\*\*\*\*\***



==================================================================



\## Example 2



```java

for(int i = 1; i <= 3; i++){



\\\&#x20;   for(int j = 1; j <= 5; j++){

\\\&#x20;       System.out.print(j);

\\\&#x20;   }



\\\&#x20;   System.out.println();

}

```



Output



**12345**

**12345**

**12345**



==================================================================



\## Example 3



```java

for(int i = 1; i <= 3; i++){



\\\&#x20;   for(int j = 1; j <= 5; j++){

\\\&#x20;       System.out.print(i);

\\\&#x20;   }



\\\&#x20;   System.out.println();

}

```



Output



**11111**

**22222**

**33333**



==================================================================



\## Example 4



```java

for(int i = 1; i <= 2; i++){



\\\&#x20;   for(int j = 1; j <= 3; j++){

\\\&#x20;       System.out.print("\\\\\\\*");

\\\&#x20;   }



\\\&#x20;   System.out.println();

}

```



Output



\*\*\*

\*\*\*



==================================================================



\## Example 5



```java

for(int i = 1; i <= 3; i++){



\\\&#x20;   for(int j = 1; j <= 2; j++){

\\\&#x20;       System.out.print(i);

\\\&#x20;   }



\\\&#x20;   System.out.println();

}

```



Output



11

22

33



==================================================================



\## Example 6



```java

for(int i = 1; i <= 4; i++){



\\\&#x20;   for(int j = 1; j <= 4; j++){

\\\&#x20;       System.out.print(i + j);

\\\&#x20;   }



\\\&#x20;   System.out.println();

}

```



Output



2345

3456

4567

5678



==================================================================













## **# 8. PATTERN PRINTING**



Print the following patterns using nested loops.



==================================================================



\### Pattern 1



\###

\###

\###

\###



==================================================================



\### Pattern 2



12345

23456

34567

45678

56789



==================================================================



\### Pattern 3



2 4 6 8 10

2 4 6 8 10

2 4 6 8 10

2 4 6 8 10

2 4 6 8 10



==================================================================



\### Pattern 4



\*

\*\*

\*\*\*

\*\*\*\*

\*\*\*\*\*



==================================================================



\### Pattern 5



\*\*\*\*\*

\*\*\*\*

\*\*\*

\*\*

\*



==================================================================



\### Pattern 6



1

12

123

1234

12345



==================================================================



\### Pattern 7



1

22

333

4444

55555



==================================================================



\### Pattern 8



54321

5432

543

54

5



==================================================================



\### Pattern 9



12345

1234

123

12

1



==================================================================



\### Pattern 10



54321

5432

543

54

5



==================================================================



\### Pattern 11



5

54

543

5432

54321



==================================================================



\### Pattern 12



5

45

345

2345

12345



==================================================================



\### Pattern 13



11111

2222

333

44

5



==================================================================



\### Pattern 14



12321

12321

12321

12321

12321



==================================================================



\### Pattern 15 (Floyd's Triangle)



Output



1

2 3

4 5 6

7 8 9 10

11 12 13 14 15



Code



```java

int num = 1;



for(int i = 1; i <= 5; i++){



\\\&#x20;   for(int j = 1; j <= i; j++){

\\\&#x20;       System.out.print(num++ + " ");

\\\&#x20;   }



\\\&#x20;   System.out.println();

}

```



==================================================================

