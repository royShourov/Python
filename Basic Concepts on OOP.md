Object-Oriented Programming (OOP) in Python is a way of structuring code so that data and behavior are bundled into **objects**. It's based on four main principles:

---

### 🔑 **Four Pillars of OOP**
1. **Encapsulation**  
   - Hiding internal state and requiring all interaction to be performed through methods.  
   - Achieved using classes and private variables/methods.

2. **Abstraction**  
   - Hiding complexity by exposing only essential features.  
   - Can use abstract base classes with `abc` module.

3. **Inheritance**  
   - Allows a class (child) to inherit attributes and methods from another class (parent).

4. **Polymorphism**  
   - Same interface, different behavior.  
   - Method overriding and duck typing in Python.

---

### 🧱 **Basic Structure**

```python
class Person:
    def __init__(self, name, age):  # Constructor
        self.name = name
        self.age = age

    def greet(self):  # Method
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

# Creating an object
p1 = Person("Alice", 25)
p1.greet()
```

---

### 🧬 **Inheritance Example**

```python
class Student(Person):  # Student inherits from Person
    def __init__(self, name, age, student_id):
        super().__init__(name, age)
        self.student_id = student_id

    def greet(self):  # Method overriding
        print(f"I'm {self.name}, a student with ID {self.student_id}.")

s1 = Student("Bob", 20, "S123")
s1.greet()
```

---

### 🔒 **Encapsulation Example**

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private variable

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance
```

---

### 🧠 **Polymorphism Example**

```python
class Dog:
    def speak(self):
        return "Woof!"

class Cat:
    def speak(self):
        return "Meow!"

def animal_sound(animal):
    print(animal.speak())  # Duck typing

animal_sound(Dog())
animal_sound(Cat())
```

---

### 🧪 **Abstract Classes**

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2
```

---
