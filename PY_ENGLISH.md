### **Python Beginner's Course - Complete Handbook**

#### **Table of Contents**

1. Introduction to Python
2. Programming Basics
3. Control Structures
4. Functions
5. Data Structures
6. Object-Oriented Programming (OOP)
7. Error Handling
8. Files and File Systems
9. Modules and Libraries
10. Projects and Applications
11. Advanced Topics
12. Additional Topics: Regular Expressions, Debugging, and Best Practices

---

### **1. Introduction to Python**

#### **What is Python?**

Python is an easy-to-learn, versatile, and popular programming language. It is used in various fields such as web development, data analysis, AI, automation, and more.

#### **Advantages of Python:**

- Easy to read and write
- Extensive standard library
- Cross-platform
- Active community

#### **Installing Python**

1. **Download**: Download Python from [python.org](https://www.python.org/).
2. **Installation**: Follow the instructions. Enable “Add Python to PATH” during installation.
3. **Verify**: Open the terminal and enter `python --version`.

#### **Recommended IDEs:**

- **VSCode**: Flexible and customizable.
- **PyCharm**: Feature-rich for Python development.
- **Jupyter Notebook**: Ideal for data analysis and scientific computing.

**First Program:**

```python
print("Hello, World!")
```

---

### **2. Programming Basics**

#### **Variables and Data Types**

Variables store data. Common data types include:

| Type     | Description     | Example         |
|----------|-----------------|-----------------|
| Integer  | Whole numbers   | `42`            |
| Float    | Decimal numbers | `3.14`          |
| String   | Text            | `'Hello'`       |
| Boolean  | Truth values    | `True`, `False` |

**Example:**

```python
name = "Alice"  # String
age = 25         # Integer
pi = 3.14        # Float
is_student = True  # Boolean
print(f"Name: {name}, Age: {age}, Student: {is_student}")
```

#### **Input and Output**

- **Input:** `input()`
- **Output:** `print()`

**Example:**

```python
username = input("What is your name? ")
print(f"Hello, {username}!")
```

---

### **3. Control Structures**

#### **Conditions (`if`, `elif`, `else`)**

**Example:**

```python
number = int(input("Enter a number: "))
if number > 0:
    print("The number is positive.")
elif number < 0:
    print("The number is negative.")
else:
    print("The number is zero.")
```

#### **Loops**

- **`for` loop:** Iterates over a sequence.
- **`while` loop:** Repeats as long as a condition is true.

**Examples:**

```python
# for loop
for i in range(1, 6):
    print(f"Number: {i}")

# while loop
x = 5
while x > 0:
    print(x)
    x -= 1
```

---

### **4. Functions**

#### **Defining Functions**

**Example:**

```python
def greeting(name):
    print(f"Hello {name}!")

greeting("Anna")
```

#### **Return Values**

```python
def add(a, b):
    return a + b

result = add(5, 7)
print(f"The sum is: {result}")
```

---

### **5. Data Structures**

#### **Lists**

Lists are ordered collections.

**Examples:**

```python
numbers = [1, 2, 3, 4, 5]
numbers.append(6)  # Add an element
numbers.remove(2)  # Remove an element
print(numbers)
```

#### **Dictionaries**

**Example:**

```python
student = {"name": "Lisa", "age": 22}
print(student["name"])
```

---

### **6. Object-Oriented Programming (OOP)**

#### **Classes and Objects**

**Example:**

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def description(self):
        return f"{self.brand} {self.model}"

my_car = Car("Tesla", "Model 3")
print(my_car.description())
```

---

### **7. Error Handling**

#### **`try` and `except`**

**Example:**

```python
try:
    number = int(input("Enter a number: "))
    print(f"Double the number is: {number * 2}")
except ValueError:
    print("Please enter a valid number!")
```

---

### **8. Files and File Systems**

#### **Reading and Writing Files**

**Example:**

```python
# Writing
with open("example.txt", "w") as file:
    file.write("Hello, file!")

# Reading
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

---

### **9. Projects and Applications**

#### **Project 1: Calculator**

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

while True:
    print("1: Add, 2: Subtract, 3: Exit")
    choice = input("Choose: ")
    if choice == "3":
        break
    num1 = float(input("First number: "))
    num2 = float(input("Second number: "))
    if choice == "1":
        print(add(num1, num2))
    elif choice == "2":
        print(subtract(num1, num2))
```

#### **Project 2: Number Guessing Game**

```python
import random
secret_number = random.randint(1, 100)
while True:
    guess = int(input("Guess the number: "))
    if guess < secret_number:
        print("Too low!")
    elif guess > secret_number:
        print("Too high!")
    else:
        print("Correct!")
        break
```

---

### **10. Advanced Topics**

#### **Data Analysis with pandas and numpy**

- **pandas**: A library for data manipulation and analysis.
- **numpy**: A powerful library for numerical computations.

**Example:**

```python
import pandas as pd
import numpy as np

# Create data with numpy
data = np.random.rand(5, 3)

# Convert data to pandas DataFrame
df = pd.DataFrame(data, columns=["A", "B", "C"])
print(df)
```

#### **Visualization with matplotlib**

- **matplotlib**: Library for creating charts and visualizations.

**Example:**

```python
import matplotlib.pyplot as plt

# Data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create plot
plt.plot(x, y, marker="o")
plt.title("Sample Plot")
plt.xlabel("x-axis")
plt.ylabel("y-axis")
plt.show()
```

#### **Web Development with Flask/Django**

- **Flask**: A lightweight web framework.
- **Django**: A full-featured web framework.

**Flask Example:**

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello, World!"

if __name__ == "__main__":
    app.run(debug=True)
```

#### **Creating GUIs with tkinter**

- **tkinter**: A standard library for creating graphical user interfaces.

**Example:**

```python
import tkinter as tk

# Create window
root = tk.Tk()
root.title("GUI Example")

# Add label
label = tk.Label(root, text="Hello, GUI!")
label.pack()

# Add button
button = tk.Button(root, text="Exit", command=root.quit)
button.pack()

# Run main loop
root.mainloop()
```

---

### **11. Additional Topics: Regular Expressions, Debugging, and Best Practices**

#### **Regular Expressions (Regex)**

Regular expressions help process text patterns.

**Example:**

```python
import re

text = "My phone number is 123-456-7890."
pattern = r"\d{3}-\d{3}-\d{4}"
match = re.search(pattern, text)
if match:
    print(f"Found number: {match.group()}")
```

#### **Debugging**

- Use `print()` statements to check variables.
- Use `pdb`, the Python debugger.

**Example:**

```python
import pdb

x = 10
y = 0
pdb.set_trace()
result = x / y
```

#### **Best Practices**

- Write clear, well-documented code.
- Use version control (e.g., Git).
- Write tests for your code.

**Example:**

```python
def square(x):
    """Calculates the square of a number."""
    return x * x

assert square(3) == 9
assert square(-4) == 16
```

