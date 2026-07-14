## ***Strings***

### ***char - utf-2***

&#x20;   ***size***

&#x20;   ***char ch     , uppercase or lowercase  , toggle case***

&#x20;   ***char ch     alphabet hai ?***

&#x20;   ***char ch      digit?***

### &#x20;

### 

### ***Strings are immutable - String constant Pool , avoiding synchronization logic***

**USING EXAMPLE FOR EACH FUNCTION**

1. String s = "John WWick"   0 to n-1 index   Literal
2. &#x20;   s3=s1.**concat**(s2)          addition                     O(n)
3. s.**charAt**(3) ?
4. s.**length**()  ?
5. s1.**compareTo**(s2)==0  same    -ve , 0 , +ve   'apple' 'banana'   , 'apple' 'Apple'
6. s1 = "hello" , s2 = "hello"  same object
7. String s1 = new **String**("Tony")   different objects here
8. String s2 = new String("Tony")   s1\*\*==\*\*s2(reference comparison) ->false   but s1.**equals**(s2) (content comparison) is true
9. &#x20;s1.**equalsIgnoreCase**(s2)
10. s1.equals(s2)   =>false

11\. s1.**substring**(5,8)             O(n)

12\. s1.**contains**("Wic");           O(n)

13\. s1.**startsWith**("John")

14\. s1.**endsWith**("Wick")

15\. s1.**indexOf**('W')     - first Occurence

16\. s1.**lastIndexOf**('i')  - last index of

17\. s1.**replace**('h','y')           O(n)

18\. s1.**toUpperCase**()

19\. s1.**toLowerCase**()

20\. s1.**trim**()  removes st and en spaces

21\. s1.**isEmpty**()

22\. s1.**split**("WW");     return array of strings     O(n)

23\. s1.**toCharArray**()    return array of characters



1. **Loop through String   for 0->n-1   print(s.charAt(i))**

**2.                       for(char c:s.toCharArray()) print(c)**

**3. Count vowels and consonants**

**4. Reverse a string         string rev ="" rev+=s.charAt(i)  O(n^2)**

**5. reverse words in a string**

**6. Longest Word in a Sentence ⭐ (Easy)**

**7. Check if Two Strings are Rotations**

## &#x20;   **=> StringBuilder**



### **Easy**

1. **Reverse String**  ✅
2. **Check if a given string is palindrome or not**  ✅
3. **Remove spaces from a string**                   ✅
4. **Remove characters from a string except alphabets**✅
5. **Find the Unicode value of a character  'A' 65-90 , 'a' 97-122**✅
6. **Frequency of Characters   <i>~~PR~~</i> -> int ch = 'a' char ch= 'm'+2  ,2+3+"hi" , "hi"+true** ✅
7. **Toggle Case**                                   ✅
8. **First Non-Repeating Character**                 ✅
9. **Sum of Digits in a Number**                     ✅    **Online java compiler**
10. **Sum of the numbers in a String**               ✅
11. **Count Words**                                  ✅
12. **Longest Word**                                 ✅
13. **Reverse Words in a String**                    ✅

### **Medium**

1. **Print Frequency of Each Character**
2. **Valid Anagram                              3.           using int\[26]**
3. **Remove Consecutive Duplicate Characters**
4. **Reverse Each Word**
5. **Longest Common Prefix                     2.**
6. **Roman to Integer                          1.**
7. **Remove Outermost Parentheses**



## **Hard**

1. **String Compression**
2. **Longest Substring Without Repeating Characters (Sliding Window)**
3. **Longest Palindromic Substring**
4. **Count Palindromic Substrings**
5. **Minimum Window Substring**

