---
title: 'Basic Python In 5 Min.'
description: 'Learn How To Code.'
pubDate: 2025-08-28
author: 'Dihan Ramanayaka'
tags: [python]
---

---

# 🐍 Python Basics for Beginners – Expanded Guide

---

## 1. Hello Python 

Python is a programming language that is **easy to read** and **beginner-friendly**.
Let’s start:

```python
print("Hello, World!")
```

👉 Prints text on the screen.

---

## 2. Variables & Data Types 

Variables are like **boxes** that store data.

```python
name = "cat"     # string (text)
age = 18           # integer (whole number)
height = 5.9       # float (decimal)
is_student = True  # boolean (True/False)
```

Check data type:

```python
print(type(name))   # <class 'str'>
```

---

## 3. Comments 

```python
# This is a comment
# Python ignores this line
```

---

## 4. Input (User Interaction) 

```python
username = input("Enter your name: ")
print("Hello,", username)
```

---

## 5. Operators 

```python
x, y = 10, 3
print(x + y)  # 13
print(x - y)  # 7
print(x * y)  # 30
print(x / y)  # 3.33
print(x // y) # 3 (floor division)
print(x % y)  # 1 (remainder)
print(x ** y) # 1000 (power)
```

---

## 6. Conditions (if/elif/else) 

```python
marks = 75
if marks >= 80:
    print("A Grade")
elif marks >= 50:
    print("Pass")
else:
    print("Fail")
```

---

## 7. Loops 

**For loop** (repeat fixed times):

```python
for i in range(5):
    print("Hi", i)
```

**While loop** (repeat until condition is false):

```python
count = 0
while count < 3:
    print("Hello")
    count += 1
```

---

## 8. Functions 

Functions are **reusable code blocks**.

```python
def greet(name):
    return "Hello, " + name

print(greet("Dihan"))
```

---

## 9. Lists 

```python
fruits = ["apple", "banana", "cherry"]
print(fruits[0])         # apple
fruits.append("mango")   # add
print(fruits)
```

---

## 10. Tuples (unchangeable list)

```python
numbers = (1, 2, 3)
print(numbers[1])  # 2
```

---

## 11. Dictionaries  (key-value pairs)

```python
student = {"name": "Dihan", "age": 18}
print(student["name"])   # Dihan
student["age"] = 19
print(student)
```

---

## 12. Sets  (unique items, no duplicates)

```python
nums = {1, 2, 3, 3}
print(nums)  # {1, 2, 3}
```

---

## 13. Strings 

```python
text = "Python"
print(text.upper())   # PYTHON
print(text.lower())   # python
print(text[0:3])      # Pyt
```

---

## 14. Importing Modules 

```python
import math
print(math.sqrt(16))  # 4.0
```

---

## 15. Error Handling 

```python
try:
    num = int("abc")   # error
except ValueError:
    print("Invalid number")
```

---

## 16. File Handling 

```python
# Write to file
with open("test.txt", "w") as f:
    f.write("Hello Python")

# Read from file
with open("test.txt", "r") as f:
    print(f.read())
```

---

#  Practice Ideas

1. Calculator
2. Guess the Number game
3. To-do list app
4. Simple quiz

---

⚡ With these basics, you can already write small programs and move on to **beginner projects**.

---
