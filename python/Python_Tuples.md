# Python Tuples

## 1. What is a Tuple?
- Ordered collection of items.  
- Immutable (cannot be changed after creation).  
- Allows duplicate values.  
- Can contain different data types.  

```python
my_tuple = ("apple", "banana", "cherry", "apple", 10, True)
print(my_tuple)  
# ('apple', 'banana', 'cherry', 'apple', 10, True)

```
------
## 2. Accessing Tuples

- Tuples use **indexing** like lists.  
- **Negative indexing** is allowed.  
- **Slicing** works too.  

```python
my_tuple = ("apple", "banana", "cherry", "apple", 10, True)

print(my_tuple[0])      # apple
print(my_tuple[-1])     # True
print(my_tuple[1:3])    # ('banana', 'cherry')
print(my_tuple[:4])     # ('apple', 'banana', 'cherry', 'apple')
print(my_tuple[::2])    # ('apple', 'cherry', 10)

```
------

## 3. Updating Tuples
- Tuples are **immutable** → you cannot directly change elements.  
- Workarounds:  
  1. Convert tuple → list → update → convert back to tuple.  
  2. Modify mutable items (like lists) inside a tuple.  

```python
# Method 1: Convert to list, update, then back to tuple
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)
print(x)   # ('apple', 'kiwi', 'cherry')

# Method 2: Modify mutable element inside tuple
t = (1, [2, 3], 4)
t[1][0] = 99
print(t)   # (1, [99, 3], 4)

```
------
## 4. Unpacking Tuples
- Assign tuple values to multiple variables.  
- Use `*` to collect multiple values.  

```python
fruits = ("apple", "banana", "cherry")
(a, b, c) = fruits
print(a)  # apple

# Using *
numbers = (1, 2, 3, 4, 5)
(a, *b, c) = numbers
print(b)  # [2, 3, 4]
```
------

## 5. Looping Through Tuples
- You can loop through tuples using different methods:  
  - `for` loop (direct iteration).  
  - `for` with `range()` (index-based).  
  - `while` loop.  

```python
fruits = ("apple", "banana", "cherry")

# For loop
for item in fruits:
    print(item)

# Index loop
for i in range(len(fruits)):
    print(i, fruits[i])

# While loop
i = 0
while i < len(fruits):
    print(fruits[i])
    i += 1
```
------

## 6. Joining Tuples
- You can **concatenate** two tuples using `+`.  
- You can **repeat** a tuple using `*`.  

```python
tuple1 = (1, 2, 3)
tuple2 = (4, 5)

# Concatenation
tuple3 = tuple1 + tuple2
print(tuple3)  # (1, 2, 3, 4, 5)

# Multiplication
tuple4 = ("hello",) * 3
print(tuple4)  # ('hello', 'hello', 'hello')
```
------

## 7. Tuple Methods
- Tuples have only two built-in methods:  
  - `count()` → returns the number of times a value appears.  
  - `index()` → returns the first index of a value.  

```python
nums = (1, 2, 2, 3, 4, 2)

print(nums.count(2))  # 3 (number of times 2 appears)
print(nums.index(3))  # 3 (first index of value 3)
```
------
## 8. Nesting Tuples
- Tuples can contain other tuples (nested structure).  
- Access elements using multiple indexes.  

```python
nested = (("a", "b"), (1, 2, 3))

print(nested[0][1])  # b
print(nested[1][2])  # 3
```
------

## 9. Tuple Packing and Unpacking
- **Packing**: putting values into a tuple.  
- **Unpacking**: extracting values into variables.  

```python
# Packing
packed = 1, 2, "apple"

# Unpacking
(a, b, c) = packed
print(a, b, c)  # 1 2 apple
```
------

## 10. Advantages of Tuples
- Faster than lists (performance benefit).  
- Can be used as dictionary keys (if fully immutable).  
- Safer (data cannot be accidentally changed).  

```python
coordinates = (10, 20)
locations = {coordinates: "My Home"}
print(locations)  # {(10, 20): 'My Home'}
```
------
## 11. Built-in Functions with Tuples
- Tuples support many built-in functions:  

```python
nums = (5, 1, 8, 3)

print(len(nums))     # 4
print(max(nums))     # 8
print(min(nums))     # 1
print(sum(nums))     # 17
print(sorted(nums))  # [1, 3, 5, 8] (returns a list)




