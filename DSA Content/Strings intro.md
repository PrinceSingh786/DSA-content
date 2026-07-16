# 🧵 Strings in Java

> 📌 **Definition**
> 
> A **String** is a sequence of characters enclosed in double quotes (`"`).

```java
String name = "John";
```

---

# 🔤 Character (`char`)

A `char` stores **a single Unicode character**.

```java
char ch = 'A';
```

### ✅ Size

- 2 bytes (UTF-16)
    

---

## Character Operations

### 🔹 Check Uppercase

```java
char ch = 'A';

if(ch >= 'A' && ch <= 'Z')
    System.out.println("Uppercase");
```

---

### 🔹 Check Lowercase

```java
char ch = 'a';

if(ch >= 'a' && ch <= 'z')
    System.out.println("Lowercase");
```

---

### 🔹 Toggle Case

```java
char ch = 'A';

if(ch >= 'A' && ch <= 'Z')
    ch = (char)(ch + 32);
else
    ch = (char)(ch - 32);
```

---

### 🔹 Check Alphabet

```java
if((ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z'))
```

---

### 🔹 Check Digit

```java
if(ch >= '0' && ch <= '9')
```

---

### 🔹 Unicode Value

```java
char ch = 'A';
System.out.println((int)ch);   //65
```

---

# 📚 Strings are Immutable

Once created, a String **cannot be changed**.

```java
String s = "Hello";

s.concat(" World");

System.out.println(s);
```

Output

```
Hello
```

Why?

`concat()` creates a **new String**.

```java
s = s.concat(" World");
```

Now

```
Hello World
```

---

# 🏊 String Constant Pool (SCP)

```java
String s1 = "Hello";
String s2 = "Hello";
```

Both point to **same object**.

```
SCP

+---------+
| Hello   |
+---------+
 ↑       ↑
s1      s2
```

---

## Using new Keyword

```java
String s1 = new String("Tony");
String s2 = new String("Tony");
```

Both create different objects.

```
Heap

+-------+     +-------+
| Tony  |     | Tony  |
+-------+     +-------+
   ↑             ↑
  s1            s2
```

---

## == vs equals()

```java
String s1 = new String("Tony");
String s2 = new String("Tony");

System.out.println(s1 == s2);
```

Output

```
false
```

Because references are different.

---

```java
System.out.println(s1.equals(s2));
```

Output

```
true
```

Because contents are same.

---

# 📖 String Functions

Assume

```java
String s = "John Wick";
```

---

## 1️⃣ length()

```java
s.length();
```

Output

```
9
```

Time → **O(1)**

---

## 2️⃣ charAt()

```java
s.charAt(2);
```

Output

```
h
```

Time → **O(1)**

---

## 3️⃣ concat()

```java
String s1="Hello ";
String s2="World";

System.out.println(s1.concat(s2));
```

Output

```
Hello World
```

Time → **O(n)**

---

## 4️⃣ compareTo()

```java
"apple".compareTo("banana")
```

Output

```
Negative
```

---

```java
"apple".compareTo("apple")
```

Output

```
0
```

---

```java
"banana".compareTo("apple")
```

Output

```
Positive
```

---

### Capital letters come first

```java
"apple".compareTo("Apple")
```

Positive because

```
'A' < 'a'
```

---

## 5️⃣ equals()

```java
"Java".equals("Java")
```

```
true
```

---

## 6️⃣ equalsIgnoreCase()

```java
"java".equalsIgnoreCase("JAVA")
```

```
true
```

---

## 7️⃣ substring()

```java
s.substring(0,4)
```

```
John
```

---

```java
s.substring(5)
```

```
Wick
```

Time → **O(n)**

---

## 8️⃣ contains()

```java
s.contains("Wic")
```

```
true
```

---

## 9️⃣ startsWith()

```java
s.startsWith("John")
```

```
true
```

---

## 🔟 endsWith()

```java
s.endsWith("Wick")
```

```
true
```

---

## 1️⃣1️⃣ indexOf()

```java
s.indexOf('W')
```

```
5
```

---

## 1️⃣2️⃣ lastIndexOf()

```java
String s="Mississippi";

System.out.println(s.lastIndexOf('i'));
```

```
10
```

---

## 1️⃣3️⃣ replace()

```java
"hello".replace('h','y')
```

```
yello
```

---

## 1️⃣4️⃣ toUpperCase()

```java
"java".toUpperCase()
```

```
JAVA
```

---

## 1️⃣5️⃣ toLowerCase()

```java
"JAVA".toLowerCase()
```

```
java
```

---

## 1️⃣6️⃣ trim()

```java
"   Java   ".trim()
```

```
Java
```

---

## 1️⃣7️⃣ isEmpty()

```java
"".isEmpty()
```

```
true
```

---

## 1️⃣8️⃣ split()

```java
String s="Java Python C++";

String arr[]=s.split(" ");
```

Output

```
Java
Python
C++
```

---

## 1️⃣9️⃣ toCharArray()

```java
char arr[]=s.toCharArray();
```

Converts String into character array.

---

# 🔁 Traversing a String

## Method 1

```java
for(int i=0;i<s.length();i++)
{
    System.out.print(s.charAt(i));
}
```

---

## Method 2

```java
for(char ch:s.toCharArray())
{
    System.out.print(ch);
}
```

---

# 🚀 StringBuilder in Java

> 📌 **StringBuilder** is a mutable sequence of characters.
> 
> ✅ Faster than `String` when performing multiple modifications like **append, insert, delete, replace, reverse**, etc.

---

# 🎯 Creating a StringBuilder

### 🔹 Empty StringBuilder

```java
StringBuilder sb = new StringBuilder();
```

Default Capacity = **16**

---

### 🔹 With Initial String

```java
StringBuilder sb = new StringBuilder("Hello");
```

Contents

```text
Hello
```

---

### 🔹 With Custom Capacity

```java
StringBuilder sb = new StringBuilder(100);
```

Capacity = **100**

Useful when you already know approximately how many characters will be stored.

---

# 📖 Common Functions

Assume

```java
StringBuilder sb = new StringBuilder("Hello");
```

---

## 1️⃣ append()

Adds text at the end.

```java
sb.append(" World");
```

Output

```text
Hello World
```

⏱ Time Complexity: **O(1)** (Amortized)

---

## 2️⃣ charAt()

Returns character at given index.

```java
sb.charAt(1);
```

Output

```text
e
```

⏱ Time Complexity: **O(1)**

---

## 3️⃣ setCharAt()

Changes a character.

```java
sb.setCharAt(1, 'a');
```

Output

```text
Hallo
```

⏱ Time Complexity: **O(1)**

---

## 4️⃣ insert()

Insert at any position.

```java
sb.insert(5, " Java");
```

Output

```text
Hello Java
```

⏱ Time Complexity: **O(n)**

---

## 5️⃣ delete()

Deletes characters from **start** to **end-1**

```java
sb.delete(1,4);
```

Example

```text
Before : Hello
After  : Ho
```

(Removes **ell**)

⏱ Time Complexity: **O(n)**

---

## 6️⃣ deleteCharAt()

Deletes one character.

```java
sb.deleteCharAt(1);
```

Output

```text
Hllo
```

⏱ Time Complexity: **O(n)**

---

## 7️⃣ replace()

Replace a range of characters.

```java
sb.replace(1,4,"abc");
```

Example

```text
Before : Hello
After  : Habco
```

(Replaces **ell** with **abc**)

⏱ Time Complexity: **O(n)**

---

## 8️⃣ reverse()

Reverse the StringBuilder.

```java
sb.reverse();
```

Output

```text
olleH
```

⏱ Time Complexity: **O(n)**

---

## 9️⃣ toString()

Converts `StringBuilder` to `String`.

```java
String s = sb.toString();
```

⏱ Time Complexity: **O(n)**

---

## 🔟 length()

Returns current number of characters.

```java
sb.length();
```

Example

```text
Hello
```

Output

```text
5
```

⏱ Time Complexity: **O(1)**

---

## 1️⃣1️⃣ capacity()

Returns total storage capacity.

```java
StringBuilder sb = new StringBuilder();
System.out.println(sb.capacity());
```

Output

```text
16
```

---

### Capacity Growth Rule

When capacity becomes full,

```text
New Capacity = (Old Capacity × 2) + 2
```

Example

```text
16 → 34 → 70 → 142 → ...
```

---

## 1️⃣2️⃣ setLength()

Changes the length.

```java
StringBuilder sb = new StringBuilder("Hello");

sb.setLength(3);
```

Output

```text
Hel
```

---

Increasing the length

```java
StringBuilder sb = new StringBuilder("Hi");

sb.setLength(5);
```

Length becomes **5**.

Remaining positions are filled with the null character (`\u0000`), which usually appears as empty when printed.

---

# 📝 Quick Revision Table

|Method|Purpose|Time|
|---|---|---|
|`append()`|Add at end|**O(1)** _(amortized)_|
|`charAt()`|Get character|**O(1)**|
|`setCharAt()`|Update character|**O(1)**|
|`insert()`|Insert characters|**O(n)**|
|`delete()`|Delete range|**O(n)**|
|`deleteCharAt()`|Delete one character|**O(n)**|
|`replace()`|Replace range|**O(n)**|
|`reverse()`|Reverse string|**O(n)**|
|`toString()`|Convert to String|**O(n)**|
|`length()`|Current length|**O(1)**|
|`capacity()`|Total capacity|**O(1)**|
|`setLength()`|Change length|**O(n)** (may resize/fill)|

---

# 💡 Why Use StringBuilder?

❌ Using `String`

```java
String s = "";

for(int i=0;i<10000;i++)
{
    s += "A";
}
```

Repeatedly creates new String objects → **Slow (≈ O(n²))**

---

✅ Using `StringBuilder`

```java
StringBuilder sb = new StringBuilder();

for(int i=0;i<10000;i++)
{
    sb.append("A");
}
```

Only one mutable object is modified → **Fast (≈ O(n))**

---

# 🎯 Interview Tip

👉 **String** → Immutable (cannot be modified)

👉 **StringBuilder** → Mutable (can be modified)

👉 Use **StringBuilder** whenever you perform many string modifications inside loops.
---

# 🎯 Beginner Practice (Level 0)

### ⭐ Character Basics

- Print a character
    
- Find Unicode value
    
- Check uppercase
    
- Check lowercase
    
- Toggle case
    
- Check alphabet
    
- Check digit
    
- Count uppercase letters
    
- Count lowercase letters
    
- Count digits
    
- Count vowels
    
- Count consonants
    
- Count special characters
    

---

### ⭐ String Basics

- Print every character
    
- Print characters with index
    
- Print string length
    
- First character
    
- Last character
    
- Middle character
    
- Count total characters
    
- Count spaces
    
- Check empty string
    
- Convert to uppercase
    
- Convert to lowercase
    
- Trim spaces
    

---

# 🟢 Easy Problems

### Basic Manipulation

- Reverse String ✅
    
- Check Palindrome ✅
    
- Remove Spaces ✅
    
- Remove All Digits
    
- Remove All Special Characters
    
- Keep Only Alphabets ✅
    
- Replace Spaces with Hyphen
    
- Replace Character
    
- Remove a Given Character
    
- Count Occurrences of a Character
    
- Find First Occurrence
    
- Find Last Occurrence
    

---

### Counting Problems

- Count Words ✅
    
- Longest Word ✅
    
- Shortest Word
    
- Count Vowels
    
- Count Consonants
    
- Count Digits
    
- Count Alphabets
    
- Count Uppercase
    
- Count Lowercase
    
- Count Special Characters
    
- Count Frequency of One Character
    
- Sum of Numbers in a String ✅
    
- Sum of Digits in a Number ✅
    

---

### Word Problems

- Reverse Words ✅
    
- Reverse Each Word
    
- Print Each Word on New Line
    
- Find Largest Word
    
- Find Smallest Word
    
- Count Words Starting with Vowel
    
- Count Words Ending with Vowel
    

---

### Comparison Problems

- Compare Two Strings
    
- Check Equal
    
- Check Equal Ignore Case
    
- Lexicographically Larger String
    
- Check Prefix
    
- Check Suffix
    
- Check Substring
    

---

# 🟡 Easy–Medium

- Print Frequency of Every Character
    
- Print Duplicate Characters
    
- Print Unique Characters
    
- Remove Duplicate Characters
    
- Remove Consecutive Duplicate Characters
    
- Most Frequent Character
    
- First Non-Repeating Character
    
- Second Most Frequent Character
    
- Sort Characters of String
    
- Check Anagram
    
- Check Rotation
    
- Check Pangram
    
- Longest Common Prefix
    
- Longest Common Suffix
    
- Reverse Only Alphabets
    
- Reverse Only Vowels
    
- Move All Digits to End
    
- Move All Alphabets to Front
    
- Compress Consecutive Characters (Basic)
    

---

# 🟠 Medium

- Roman to Integer
    
- Integer to Roman
    
- Remove Outermost Parentheses
    
- Valid Parentheses
    
- Decode String (Basic)
    
- String Compression
    
- Isomorphic Strings
    
- Group Anagrams
    
- Multiply Large Numbers (Strings)
    
- Add Large Numbers (Strings)
    
- Compare Version Numbers
    
- Zigzag Conversion
    
- Count and Say
    
- Implement `atoi()`
    
- Implement `strStr()`
    

---

# 🔴 Hard

- Longest Substring Without Repeating Characters ⭐
    
- Minimum Window Substring ⭐
    
- Longest Palindromic Substring ⭐
    
- Count Palindromic Substrings ⭐
    
- Edit Distance
    
- Wildcard Matching
    
- Regular Expression Matching
    
- Minimum Insertions to Make Palindrome
    
- Shortest Palindrome
    
- Rabin-Karp
    
- KMP Algorithm
    
- Z Algorithm
    
- Rolling Hash
    
- Suffix Array (Advanced)
    

---

# 📌 Recommended Teaching Order

```text
Characters
        ↓
Basic String Functions
        ↓
Traversal
        ↓
StringBuilder
        ↓
Reverse String
        ↓
Palindrome
        ↓
Counting Problems
        ↓
Word Problems
        ↓
Frequency Problems
        ↓
Anagram
        ↓
Rotation
        ↓
Longest Common Prefix
        ↓
Parentheses Problems
        ↓
Sliding Window
        ↓
Advanced Algorithms (KMP, Rabin-Karp)
```

---

# 🎯 Must Do Before Placements

✅ Reverse String

✅ Palindrome

✅ Count Characters

✅ Frequency

✅ Reverse Words

✅ Remove Duplicates

✅ Anagram

✅ Rotation

✅ Longest Common Prefix

✅ Roman to Integer

✅ String Compression

✅ Longest Substring Without Repeating Characters

✅ Minimum Window Substring

✅ Longest Palindromic Substring