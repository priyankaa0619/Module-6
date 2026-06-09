# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
```
from abc import ABC, abstractmethod

# Abstract class
class Shape(ABC):
    
    @abstractmethod
    def calculate_area(self):
        pass


# Rectangle class
class Rectangle(Shape):
    def __init__(self, length=5, breadth=3):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        return self.length * self.breadth


# Circle class
class Circle(Shape):
    def __init__(self, radius=4):
        self.radius = radius

    def calculate_area(self):
        return 3.14 * self.radius * self.radius


# Create objects
r = Rectangle()
c = Circle()

# Display results
print("Rectangle Area:", r.calculate_area())
print("Circle Area:", c.calculate_area())
```
## Output
<img width="568" height="356" alt="image" src="https://github.com/user-attachments/assets/7581f678-fb66-403f-81cc-cc405b27a0a2" />


## Result
The program was executed successfully. An abstract class with an abstract method was created and implemented in subclasses to calculate the area of different shapes
