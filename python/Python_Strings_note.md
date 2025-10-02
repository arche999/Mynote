# Python Strings

## Creating Strings
```python
Slicing Strings

text = "Hello, World!"
print(text[0:5])   # 'Hello'
print(text[-6:])   # 'World!'

Modify Strings

text = " Hello, World! "
print(text.strip())   # remove whitespace
print(text.lower())   # lowercase
print(text.upper())   # uppercase
print(text.replace("H", "J"))  # 'Jello, World!'

Concatenate Strings

a = "Hello"
b = "World"
print(a + " " + b)   # 'Hello World'

Format Strings

age = 25
txt = f"My age is {age}"
print(txt)   # 'My age is 25'

Escape Characters

txt = "We are the so-called \"Vikings\" from the north."

Common String Methods

text = "hello world"
print(len(text))        # length
print(text.capitalize()) # 'Hello world'
print(text.title())      # 'Hello World'
print(text.find("world"))# index = 6
print(text.split())      # ['hello', 'world']
print(text.join(["a","b"])) # 'ahelloworldb'
print(text.startswith("he")) # True
print(text.endswith("ld"))   # True

