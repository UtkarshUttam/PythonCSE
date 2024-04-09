# Conditions
 - Boolean Logic:
    - > 
    - <
    - ==
    - !=
    - >=
    - <=
 - Logical operators:
    - and
    - or
    - not
 - ranges
    - range(start, stop, step)
    ```Python
    {
        x = range(3,6)
        for n in x:
            print(n)
    }
    ```
 - Control statements:
    - if - else:
    ```Python
    {
        if(hour<18>):
            greeting = "Good day";
        else:
            greeting = "Good evening";

    }
    ```
    - if - elif - else:
    ```Python
    {
        a = 200
        b = 33
        if b>a:
            print("b is greater than a")
        elif a==b:
            print("a and b are equal")
        else:
            print("a is greater than b")

    }
    ```
- loops:
    - while loop
    ```Python
    {
        i = 1
        while i<6:
            print(i)
            i += 1
    }
    ```
    
    - for loop
    ```Python
    {
        for x in "banana":
            print(x)
    }
    ```





### Functions
```python
def greet(name):
    return "Hello, " + name + "!"

print(greet("Alice"))
```

### Scoping
```python
x = 10

def foo():
    x = 20
    print("Inside foo:", x)

foo()
print("Outside foo:", x)
```

### Exceptions
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

### Input and Output
```python
name = input("Enter your name: ")
print("Hello,", name)
```

### Modules
```python
# Save this code in a file named "my_module.py"
def greet(name):
    return "Hello, " + name + "!"

# Use the module in another file
import my_module
print(my_module.greet("Alice"))
```

### Collections
```python
numbers = [1, 2, 3, 4, 5]
print(numbers)
```

### Lists
```python
fruits = ["apple", "banana", "orange"]
print(fruits[0])
```

### Tuples
```python
point = (10, 20)
print(point[0])
```

### Sets
```python
my_set = {1, 2, 3, 4, 5}
print(my_set)
```

### Dictionaries
```python
person = {"name": "Alice", "age": 30}
print(person["name"])
```

### Modules
```python
# Importing the math module
import math
print(math.sqrt(25))
```

### Standard Modules
```python
import random
print(random.randint(1, 100))
```

### Regular Expressions
```python
import re
pattern = r"world"
text = "Hello, world!"
match = re.search(pattern, text)
print(match.group())
```

### Quantifiers
```python
import re
pattern = r"ca+t"
text = "cat, caat, caaat"
matches = re.findall(pattern, text)
print(matches)
```

### Basic String Operations
```python
text = "Hello, world!"
print(text.upper())
print(text.lower())
print(text.startswith("Hello"))
```






# Unit - 3:

Certainly! Here are code snippet examples for each topic in Markdown format:

### Principles of Object Orientation
```python
# Encapsulation: Combining data and methods that operate on the data within a single unit.
# Inheritance: Creating new classes by extending existing classes, inheriting their attributes and methods.
# Polymorphism: Objects of different classes can be treated as objects of a common superclass.
```

### Classes in Python
```python
# Define a simple class named Person
class Person:
    pass
```

### Creating Classes
```python
# Define a class with attributes and methods
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def display_info(self):
        return f"{self.make} {self.model}"
```

### Instance Methods
```python
# Define a class with instance methods
class Circle:
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

    def circumference(self):
        return 2 * 3.14 * self.radius
```

### Access Specification
```python
# Define a class with public, protected, and private attributes
class MyClass:
    def __init__(self):
        self.public_attribute = "Public"
        self._protected_attribute = "Protected"
        self.__private_attribute = "Private"
```

### Data Modeling
```python
# Define a class to model a student
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

### Persistent Storage of Objects
```python
# Define a class and methods to handle object serialization
import pickle

class MyClass:
    def __init__(self, data):
        self.data = data

    def save_to_file(self, filename):
        with open(filename, 'wb') as f:
            pickle.dump(self, f)

    @classmethod
    def load_from_file(cls, filename):
        with open(filename, 'rb') as f:
            return pickle.load(f)
```

### Inheritance
```python
# Define a base class and a derived class
class Animal:
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"
```

### Polymorphism
```python
# Define a class and demonstrate polymorphism
class Shape:
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height
```

### Operator Overloading
```python
# Define a class and overload the addition operator
class ComplexNumber:
    def __init__(self, real, imaginary):
        self.real = real
        self.imaginary = imaginary

    def __add__(self, other):
        real_part = self.real + other.real
        imaginary_part = self.imaginary + other.imaginary
        return ComplexNumber(real_part, imaginary_part)
```



# UNIT 3

Certainly! Here are code snippet examples for each topic in Markdown format:

### A Brief History of Python
```python
# Guido van Rossum created Python in the late 1980s.
# First released in 1991, Python's design philosophy emphasizes code readability.
# Python is named after the British comedy group Monty Python.
```

### Different Versions
```python
# Python 2: Legacy version, discontinued support since January 1, 2020.
# Python 3: Latest version, backward-incompatible with Python 2.
```

### Python 2 vs Python 3


| Feature                   | Python 2                                                | Python 3                                               |
|---------------------------|---------------------------------------------------------|--------------------------------------------------------|
| Print Statement           | ```print "Hello, World!"```                             | ```print("Hello, World!")```                            |
| Integer Division          | ```5 / 2  # Result: 2```                                | ```5 / 2  # Result: 2.5```                             |
| Unicode Handling          | Limited support for Unicode, `unicode` and `str` types  | Full Unicode support, `str` for Unicode, `bytes` for binary data |
| `xrange()` vs `range()`  | `xrange()` returns an xrange object (lazy sequence)     | `range()` returns a generator-like object in Python 3    |
| Exception Handling Syntax | ```except Exception, e:```                             | ```except Exception as e:```                           |
| `__future__` Imports      | Some features require importing from `__future__`       | Many of the future features are default in Python 3     |
| `input()` Function        | `input()` interprets input as Python code                | `input()` returns a string, `raw_input()` replaced by `input()`  |
| `unicode` Literals        | `u"Hello"`                                              | `"Hello"` or `u"Hello"` for Unicode strings             |
| Iterators and `next()`    | `next()` method for iterators and generators            | `next()` built-in function for iterators and generators |


```python
# Python 2: print statement, integer division, limited Unicode support.
# Python 3: print() function, true division, full Unicode support.
```

### Installing Python
```python
# Download Python from python.org and run the installer.
# Make sure to check the option to add Python to PATH during installation.
# Verify installation by running `python --version` in the command line.
```

### Environment Variables
```python
# Set PYTHONPATH environment variable to specify additional directories to search for Python modules.
# Example: export PYTHONPATH=/path/to/your/modules
```

### Executing Python from the Command Line
```python
# Run a Python script: python script.py
# Run Python in interactive mode: python
# Execute a single command: python -c "print('Hello, world!')"
```

### Editing Python Files
```python
# Use any text editor such as VS Code, Sublime Text, or Atom.
# Save the file with a .py extension, e.g., myscript.py.
```

### Basic Python Syntax
```python
# Python uses indentation to define code blocks.
# Example:
if True:
    print("This is indented code.")
```

### String Values
```python
# Define string variables using single or double quotes.
name = 'Alice'
greeting = "Hello, " + name
print(greeting)
```

### String Operators
```python
# Concatenate strings using the + operator.
# Example:
first_name = "John"
last_name = "Doe"
full_name = first_name + " " + last_name
print(full_name)
```

### Numeric Data Types Conversions
```python
# Convert strings to integers or floats using int() and float() functions.
# Example:
num_str = "10"
num_int = int(num_str)
print(num_int)
```

### Simple Input and Output
```python
# Get user input using the input() function.
name = input("Enter your name: ")
print("Hello,", name)
```

### Language components - Control Flow structures and Syntax - Relational Operators - Logical Operators - Bit Wise Operators
```python
# Control Flow structures:
# if-else, for loop, while loop

# Relational Operators:
# ==, !=, <, >, <=, >=

# Logical Operators:
# and, or, not

# Bit Wise Operators:
# &, |, ^, ~, <<, >>
```

### Python for Windows
```python
# Install Python for Windows from python.org.
# Use Python executable and command prompt for Windows-specific development.
```
