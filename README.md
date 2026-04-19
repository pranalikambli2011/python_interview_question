Here’s a clean **GitHub README.md format** for your Python interview prep 👇

---

# 🐍 Python Interview Questions & Answers

A curated list of commonly asked Python interview questions with examples and explanations.

---

## 📌 Table of Contents

* OOP Concepts
* Python Coding Questions
* File Handling
* Error Handling
* API Handling
* Core Python Concepts

---

## 🔹 1. OOP Concepts

### Encapsulation

Encapsulation is the concept of wrapping data and methods into a single unit and restricting access.

```python
class Person:
    def __init__(self, name):
        self.__name = name

    def get_name(self):
        return self.__name
```

---

### Inheritance

Allows one class to inherit properties of another.

```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    pass
```

---

### Polymorphism

Same method behaves differently.

```python
class Dog:
    def speak(self):
        print("Bark")

class Cat:
    def speak(self):
        print("Meow")
```

---

### Method Overriding

```python
class Animal:
    def speak(self):
        print("Animal sound")

class Dog(Animal):
    def speak(self):
        print("Bark")
```

---

### Class vs Static Method

```python
class Demo:
    @classmethod
    def class_method(cls):
        print("Class method")

    @staticmethod
    def static_method():
        print("Static method")
```

---

## 🔹 2. Python Coding Questions

### Remove Duplicates

```python
lst = [1,2,3,3,4,4]
result = list(set(lst))
```

---

### Flatten Nested List

```python
def flatten(lst):
    result = []
    for i in lst:
        if isinstance(i, list):
            result.extend(flatten(i))
        else:
            result.append(i)
    return result
```

---

### Second Largest Number

```python
lst = [10,20,4,45,99]
lst = list(set(lst))
lst.sort()
print(lst[-2])
```

---

### Merge Dictionaries

```python
d1 = {'a':1}
d2 = {'b':2}
result = {**d1, **d2}
```

---

### Frequency Count

```python
lst = [1,1,2,3,3,3]
freq = {}

for i in lst:
    freq[i] = freq.get(i, 0) + 1
```

---

### Sort Dictionary by Value

```python
D = {'a':3,'b':1,'c':2}
sorted_dict = dict(sorted(D.items(), key=lambda x: x[1]))
```

---

## 🔹 3. File Handling

### Read File

```python
with open("file.txt") as f:
    for line in f:
        print(line.strip())
```

---

### Write File

```python
with open("file.txt", "w") as f:
    f.write("Hello")
```

---

### Count Lines

```python
with open("file.txt") as f:
    print(sum(1 for _ in f))
```

---

### Large File Handling

```python
with open("file.txt") as f:
    for line in f:
        process(line)
```

---

## 🔹 4. Error Handling

### Try-Except

```python
try:
    x = 10/0
except ZeroDivisionError:
    print("Error")
```

---

### Multiple Exceptions

```python
try:
    x = int("abc")
except (ValueError, TypeError):
    print("Error")
```

---

### Finally Block

```python
try:
    pass
finally:
    print("Always runs")
```

---

### Custom Exception

```python
class MyError(Exception):
    pass

raise MyError("Custom error")
```

---

## 🔹 5. API Handling

### GET Request

```python
import requests
res = requests.get("https://api.example.com")
```

---

### POST Request

```python
requests.post("url", json={"key":"value"})
```

---

### Error Handling

```python
if res.status_code != 200:
    print("Error")
```

---

### Timeout

```python
requests.get("url", timeout=5)
```

---

### Parse JSON

```python
data = res.json()
```

---

## 🔹 6. Core Python Concepts

### List vs Tuple

| Feature | List | Tuple |
| ------- | ---- | ----- |
| Mutable | Yes  | No    |
| Syntax  | []   | ()    |

---

### Deep Copy vs Shallow Copy

```python
import copy

a = [[1,2]]
b = copy.copy(a)
c = copy.deepcopy(a)
```

---

### GIL (Global Interpreter Lock)

* Only one thread executes Python bytecode at a time

---

### Generator vs List
| Feature      | List                     | Generator                     |
| ------------ | ------------------------ | ----------------------------- |
| Memory Usage | High (stores all values) | Low (one value at a time)     |
| Execution    | Immediate                | Lazy (on demand)              |
| Speed        | Faster for small data    | Better for large data         |
| Syntax       | `[]`                     | `()`                          |
| Reusability  | Can reuse multiple times | Exhausted after one iteration |

```python
# List
l = [i for i in range(5)]

# Generator
g = (i for i in range(5))
```

---

### Memory Management

* Python uses its private heap space to manage the memory. Basically, all the objects and data structures are stored in the private heap space. Even the programmer can not access this private space as the interpreter takes care of this space. Python also has an inbuilt garbage collector, which recycles all the unused memory and frees the memory and makes it available to the heap space.



---

## 🔹 7. Common Errors

### Adding String and Number

```python
a = 5
b = "abc"

# TypeError
print(str(a) + b)
```

---

### Adding Strings

```python
a = "test"
b = "test1"

print(a + b)
```

---
