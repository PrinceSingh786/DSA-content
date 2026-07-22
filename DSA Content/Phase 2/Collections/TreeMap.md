# 🌳 Java Collections Framework – TreeMap

> **Language:** Java  
> **Prerequisite:** HashMap, Binary Search Tree (BST)

---

# 📖 What is TreeMap?

A **TreeMap** stores **key-value pairs** in **sorted order of keys**.

- ✅ Keys are automatically sorted
- ✅ No duplicate keys
- ✅ Values can be duplicated
- ❌ No null keys
- ✅ One or more null values allowed

Internally, TreeMap uses a **Red-Black Tree (Self-Balancing BST)**.

---

# 📖 Import

```java
import java.util.TreeMap;
```

---

# 📖 Creating TreeMap

```java
TreeMap<Integer, String> map = new TreeMap<>();
```

---

# 📖 Basic Methods

## put()

```java
map.put(101, "Prince");
map.put(103, "Rahul");
map.put(102, "Aman");
```

Output

```text
{101=Prince, 102=Aman, 103=Rahul}
```

---

## get()

```java
System.out.println(map.get(102));
```

---

## remove()

```java
map.remove(103);
```

---

## containsKey()

```java
map.containsKey(101);
```

---

## containsValue()

```java
map.containsValue("Prince");
```

---

## firstKey()

```java
map.firstKey();
```

Returns smallest key.

---

## lastKey()

```java
map.lastKey();
```

Returns largest key.

---

## higherKey()

```java
map.higherKey(102);
```

Returns next greater key.

---

## lowerKey()

```java
map.lowerKey(102);
```

Returns previous smaller key.

---

## ceilingKey()

```java
map.ceilingKey(102);
```

Smallest key ≥ 102

---

## floorKey()

```java
map.floorKey(102);
```

Largest key ≤ 102

---

## size()

```java
map.size();
```

---

## clear()

```java
map.clear();
```

---

## isEmpty()

```java
map.isEmpty();
```

---

# 📖 Traversal

```java
for(Map.Entry<Integer,String> entry : map.entrySet())
{
    System.out.println(entry.getKey() + " " + entry.getValue());
}
```

---

# 📖 Time Complexity

| Operation | Complexity |
|-----------|------------|
| put() | O(log n) |
| get() | O(log n) |
| remove() | O(log n) |
| containsKey() | O(log n) |
| firstKey() | O(log n) |
| lastKey() | O(log n) |

---

# 📖 HashMap vs TreeMap

| HashMap | TreeMap |
|----------|----------|
| Random Order | Sorted Order |
| O(1) Average | O(log n) |
| Allows One Null Key | No Null Keys |
| Hash Table | Red-Black Tree |

---

# 📖 Applications

- Leaderboards
- Phone Directory
- Dictionary
- Calendar Booking
- Ranking Systems
- Scheduling

---

# 📖 Practice Problems

### Easy

1. Store Student Marks
2. Phone Directory
3. Frequency of Characters
4. Find Highest Key
5. Find Lowest Key

### Medium

6. My Calendar I
7. Exam Room
8. Contains Duplicate III
9. Ordered Stream
10. Leaderboard

---

# 📖 Common Interview Questions

1. Difference between HashMap and TreeMap?
2. Why is TreeMap slower than HashMap?
3. Can TreeMap have duplicate keys?
4. Can TreeMap have null keys?
5. What data structure is used internally?

---

# 📖 Key Points

- ✅ Stores **key-value pairs**
- ✅ Keys are **sorted automatically**
- ✅ Duplicate keys are **not allowed**
- ✅ Implemented using **Red-Black Tree**
- ✅ All major operations take **O(log n)**