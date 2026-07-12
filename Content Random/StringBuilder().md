# StringBuilder()



1. StringBuilder sb = new **StringBuilder**();
2. StringBuilder sb = new **StringB  uilder**(100);  capacity
3. sb.**setCharAt**(3,'Y')                    O(1)
4. sb.**charAt**(index)                       O(1)
5. sb.**append**("Henry")                     O(1)
6. &#x20;sb.**insert**(1,"English")                O(n)
7. &#x20;sb.**delete**(1,4);
8. &#x20;sb.**deleteCharAt**(1);                   O(n)  
9. &#x20;sb.**reverse**();                         O(n)
10. sb.**replace**(1,4,"abc")                 O(n)
11. sb.**toString**()                         O(n)
12. sb.**length**()                           O(n)
13. sb.**capacity**()      default - 16  j                2\*x+2
14. sb.**setLength**(3)   sb= "hello"  , set ->  "hel"







