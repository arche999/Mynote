# Python Strings

Strings in Python are sequences of characters enclosed in single quotes `'`, double quotes `"`, or triple quotes `'''` / `"""`.

---

```python
Strings

text = "Hello, World!"
print(text)  
# Output: Hello, World!
# Explanation: A string is created using double quotes.

Slicing

print(text[0:5])   # Output: Hello
# Explanation: Extract characters from index 0 to 4.
print(text[-6:])   # Output: World!
# Explanation: Negative index counts from the end.


Modify Strings

print(text.strip())         
# Output: Hello, World!
# Explanation: strip() removes spaces at the beginning and end.

print(text.lower())         
# Output: hello, world!
# Explanation: lower() converts all characters to lowercase.

print(text.upper())         
# Output: HELLO, WORLD!
# Explanation: upper() converts all characters to uppercase.

print(text.replace("H","J"))
# Output: Jello, World!
# Explanation: replace() substitutes "H" with "J".


Concatenate

a = "Hello"
b = "World"
print(a + " " + b)   
# Output: Hello World
# Explanation: The + operator joins strings. Add " " for spacing.


Format Strings

age = 25
print(f"My age is {age}")   
# Output: My age is 25
# Explanation: f-strings let you embed variables inside {}.


Escape Characters

txt = "We are the so-called \"Vikings\" from the north."
print(txt)
# Output: We are the so-called "Vikings" from the north.
# Explanation: Use \" to include double quotes inside a string.


String Methods

sample = "hello world"

print(len(sample))          
# Output: 11
# Explanation: len() gives the number of characters.

print(sample.capitalize())  
# Output: Hello world
# Explanation: capitalize() makes the first letter uppercase.

print(sample.title())       
# Output: Hello World
# Explanation: title() makes each word start with uppercase.

print(sample.find("world")) 
# Output: 6
# Explanation: find() returns the starting index of substring.

print(sample.split())       
# Output: ['hello', 'world']
# Explanation: split() breaks string into a list of words.

print(" ".join(["a","b"]))  
# Output: a b
# Explanation: join() merges list elements with separator " ".

print(sample.startswith("he")) 
# Output: True
# Explanation: startswith() checks if string begins with given text.

print(sample.endswith("ld"))   
# Output: True
# Explanation: endswith() checks if string ends with given text.
