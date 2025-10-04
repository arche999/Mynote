# Python Lists 

## What is a List
- A **List** is one of Python’s 4 built-in collection data types (others: Tuple, Set, Dictionary).  
- Features: **ordered**, **mutable (changeable)**, allows **duplicate elements**.  

```python
fruits = ["apple", "banana", "cherry"]   # list of strings
numbers = [1, 2, 3, 4, 5]                # list of numbers
mixed = ["apple", 1, True, 3.14]         # mixed types
```
----
## Access List Items

- **Index starts at 0.**  
- **Negative indexes** count from the end.  
- **Slicing** returns a sub-list.  

### Examples

```python
fruits = ["apple", "banana", "cherry", "date"]

# index
print(fruits[0])      # "apple"
print(fruits[2])      # "cherry"

# negative index
print(fruits[-1])     # "date"
print(fruits[-2])     # "cherry"

# slicing (start inclusive, end exclusive)
print(fruits[1:3])    # ["banana", "cherry"]
print(fruits[:2])     # ["apple", "banana"]
```
----
## Change List Items

- **Lists are mutable.** You can directly update an element.  

### Examples

```python
fruits = ["apple", "banana", "cherry"]

# change value at index 1
fruits[1] = "blueberry"
print(fruits)  # ["apple", "blueberry", "cherry"]
```
----

## Add Items

- **append()** adds an item at the end.  
- **insert()** adds an item at a specific index.  

### Examples

```python
fruits = ["apple", "banana", "cherry"]

# add at the end
fruits.append("orange")

# add at index 1
fruits.insert(1, "grape")

print(fruits)  
# ["apple", "grape", "banana", "cherry", "orange"]

```
----

## Remove Items

- **remove(value)** deletes by value.  
- **pop(index)** deletes by index (default: last).  
- **del** deletes an item or the whole list.  
- **clear()** empties the list.  

### Examples

```python
fruits = ["apple", "banana", "cherry", "date"]

# remove by value
fruits.remove("apple")   

# remove first element
fruits.pop(0)            

# delete element at index 1
del fruits[1]            

# empty the list
fruits.clear()   
```
----

## Loop Through a List

- Use a **for loop** to access each item.  
- Each iteration gives you one element from the list.  

### Examples

```python
fruits = ["apple", "banana", "cherry"]

# simple loop
for item in fruits:
    print(item)
# Output:
# apple
# banana
# cherry

# loop with index
for i in range(len(fruits)):
    print(i, fruits[i])
# Output:
# 0 apple
# 1 banana
# 2 cherry

```
----
## List Comprehension

- Compact way to create lists.  
- Often used as a shortcut for loops.  
- Can include conditions for filtering.  

### Examples
```python
# squares
squares = [x**2 for x in range(5)]
print(squares)  
# [0, 1, 4, 9, 16]

# filtering even numbers
evens = [x for x in range(10) if x % 2 == 0]
print(evens)  
# [0, 2, 4, 6, 8]

# with condition and transformation
words = ["apple", "banana", "cherry"]
short_words = [w.upper() for w in words if len(w) <= 5]
print(short_words)  
# ["APPLE"]
```
----
## Sort Lists

- **sort()** sorts ascending (default).  
- **sort(reverse=True)** sorts descending.  
- **sorted(list)** returns a new sorted list without modifying the original.  

### Examples
```python
nums = [3, 1, 4, 2]

# ascending
nums.sort()
print(nums)  
# [1, 2, 3, 4]

# descending
nums.sort(reverse=True)
print(nums)  
# [4, 3, 2, 1]

# using sorted (does not modify original)
nums = [3, 1, 4, 2]
sorted_nums = sorted(nums)
print(sorted_nums)  
# [1, 2, 3, 4]

```
----

## Copy Lists

- Do not use `=` because it creates a reference, not a copy.  
- Use **copy()** or **list()** for a real shallow copy.  

### Examples
```python
fruits = ["apple", "banana", "cherry"]

# copy using copy()
copy1 = fruits.copy()

# copy using list()
copy2 = list(fruits)

# both are independent copies
print(copy1)  
# ["apple", "banana", "cherry"]

print(copy2)  
# ["apple", "banana", "cherry"]
```
----
## Join Lists

- Use **+** to concatenate two lists.  
- Use **extend()** to add elements from another list.  

### Examples
```python
a = [1, 2]
b = [3, 4]

# concatenate with +
c = a + b
print(c)  
# [1, 2, 3, 4]

# extend list a with elements of b
a.extend(b)
print(a)  
# [1, 2, 3, 4]
```
----
## Common List Methods (Cheat Sheet)

| Method      | Description                        | Example                                |
|-------------|------------------------------------|----------------------------------------|
| append(x)   | Add an item at the end             | `fruits.append("apple")`               |
| extend(x)   | Add elements from another list     | `fruits.extend(["grape", "melon"])`    |
| insert(i,x) | Insert item at index i             | `fruits.insert(1, "pear")`             |
| remove(x)   | Remove the first occurrence of x   | `fruits.remove("apple")`               |
| pop(i)      | Remove and return item at index i  | `fruits.pop(0)`                        |
| clear()     | Remove all items                   | `fruits.clear()`                       |
| sort()      | Sort ascending                     | `nums.sort()`                          |
| reverse()   | Reverse order of list              | `fruits.reverse()`                     |
| copy()      | Return a shallow copy              | `copy_list = fruits.copy()`            |
| count(x)    | Count how many times x appears     | `fruits.count("apple")`                |
| index(x)    | Return index of first occurrence   | `fruits.index("banana")`               |




