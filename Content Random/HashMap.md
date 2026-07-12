# **HashMap** =   sorted and unique keys

&#x20;       key - > value

&#x20;       HashMap<Integer,String> map = new HashMap<>();

1. &#x20;          map.put(1,"aman")
2. &#x20;          map.put(2,"rajiv")
3. &#x20;          map.get()  key
4. &#x20;          map.containsKey(4)   key     true or falsee
5. &#x20;          map.containsValue("David")
6. &#x20;          map.remove(2)
7. &#x20;          map.size()
8. &#x20;          map.isEmpty()
9. &#x20;          map.clear()
10. &#x20;         map.getOrDefault(key)
11. &#x20;         map.putIfAbsent(sum , i)







### **Time Complexities**

Method	                      Average Worst 	Explanation

1. put(key, value)  	    O(1)	O(n)	Insert or update a key-value pair
2. get(key)	            O(1)	O(n)	Find value using the key
3. containsKey(key)	    O(1)	O(n)	Checks if a key exists
4. containsValue(value)	    O(n)	O(n)	Must scan all values because values are not hashed
5. remove(key)	            O(1)	O(n)	Removes the key-value pair
6. size()	            O(1)	O(1)	Returns the stored count
7. isEmpty()	            O(1)	O(1)	Checks if size is 0
8. clear()	            O(n)	O(n)	Removes all entries
9. getOrDefault(key, defaultValue O(1)	O(n)	Returns the value or the default if the key doesn't exist



&#x20;

#### **Traverse**

1. &#x20;                            for(Integer key:map.keySet())
2. &#x20;                            for(String values:map.values()
3. &#x20;                            for(Map.Entry<Integer,String> e:map.entrySet())

&#x20;                                         e.getKey()  , e.getValue()

&#x20;



&#x20;

### **LEVEL O**

1. Create a Student Map (roll -> name) Print all students map
2. Search a Student   Given a roll number, print the student's name.  If not found, print "Student Not Found".
3. Update a Student Name     Given a roll number



