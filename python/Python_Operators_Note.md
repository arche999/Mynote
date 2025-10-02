# Python Operators – Explained with Examples

Operators perform operations on variables and values.

---

## 1. Arithmetic Operators  
Used with numbers for basic math.  
```python
x, y = 10, 3

print(x + y)   # 13 → addition
print(x - y)   # 7  → subtraction
print(x * y)   # 30 → multiplication
print(x / y)   # 3.333 → division (always float)
print(x % y)   # 1  → remainder of 10 ÷ 3
print(x ** y)  # 1000 → 10^3 (exponent)
print(x // y)  # 3 → floor division (rounds down)
```

---

## 2. Assignment Operators  
Assign or update variable values.  
```python
x = 5        # assign 5
x += 3       # x = 8  (add and assign)
x -= 2       # x = 6  (subtract and assign)
x *= 4       # x = 24 (multiply and assign)
x //= 5      # x = 4  (floor divide and assign)
x **= 2      # x = 16 (exponentiate and assign)

# Bitwise assignment
x &= 7       # x = x & 7
x |= 2       # x = x | 2

# Walrus operator (assign inside expression)
print(x := 3)  # prints 3 and assigns x = 3
```

---

## 3. Comparison Operators  
Compare values. Always return `True` or `False`.  
```python
x, y = 5, 10
print(x == y)   # False (equal?)
print(x != y)   # True  (not equal?)
print(x > y)    # False (greater?)
print(x < y)    # True  (less?)
print(x >= 5)   # True  (greater or equal)
print(y <= 10)  # True  (less or equal)
```

---

## 4. Logical Operators  
Combine conditions.  
```python
x, y = 5, 10

print(x < 10 and y > 5)  # True (both true)
print(x < 4 or y > 5)    # True (at least one true)
print(not(x < 10))       # False (negates the result)
```

---

## 5. Identity Operators  
Check if two variables refer to the **same object in memory**.  
```python
a = [1, 2]
b = a
c = [1, 2]

print(a is b)      # True (same object reference)
print(a is not c)  # True (different objects, same value)
```

---

## 6. Membership Operators  
Check if a value exists in a sequence (list, string, tuple).  
```python
nums = [1, 2, 3]

print(2 in nums)       # True (2 is inside list)
print(4 not in nums)   # True (4 is not inside list)

text = "hello"
print("h" in text)     # True
print("z" not in text) # True
```

---

## 7. Bitwise Operators  
Work on numbers at the **binary level** (0 and 1).  
```python
x, y = 6, 3   # 6 = 110 (binary), 3 = 011

print(x & y)   # 2 → AND (only 1 if both are 1)
print(x | y)   # 7 → OR  (1 if either is 1)
print(x ^ y)   # 5 → XOR (1 if only one is 1)
print(~x)      # -7 → NOT (flips all bits)
print(x << 1)  # 12 → shift left (adds 0 at right)
print(x >> 1)  # 3 → shift right (drops right bit)
