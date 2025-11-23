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
rom abc import ABC,abstractmethod
class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass
class Rectangle(Shape):
    length = 5
    breadth =3 
    def calculate_area(self):
        return self.length * self.breadth

class Circle(Shape):
    radius = 4
    def calculate_area(self):
        return 3.14 * self.radius * self.radius
rec=Rectangle()
cir=Circle()

print("Area of a rectangle:", rec.calculate_area()) #call to 'calculate_area' method defined inside the class 'Rectangle'
print("Area of a circle:", cir.calculate_area()) #call to 'calculate_area' method defined inside the class 'Circle'.
```
## Output
<img width="907" height="189" alt="image" src="https://github.com/user-attachments/assets/1b7755fd-15c1-495b-a682-be396c13ce3c" />


## Result
Thus the program to create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle is executed successfully.

# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
```
class Rectangle:
    def __init__(self,length,breadth):
        self.__length = length #private variable
        self.__breadth = breadth#private variable
    def display(self):
        print(self.__length)
        print(self.__breadth)
 
rect = Rectangle(5,3)
rect.display()


```
## Output
<img width="920" height="216" alt="image" src="https://github.com/user-attachments/assets/7abee980-32f2-4dae-b5a0-c4dcb82fced3" />


## Result
Thus the program to implement Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth is executed successfully

# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
    def type(self):
        print("shark")

obj_gold=Fish()
obj_hammer=Shark()

for inf in(obj_gold,obj_hammer):
    inf.type()

```
## OUTPUT
<img width="1000" height="184" alt="image" src="https://github.com/user-attachments/assets/48bce1d1-7341-4fb0-b19f-ac36cc2efb60" />


## RESULT
Thus the program that demonstrates class inheritance by creating a parent class Fish with a method type, and a child class Shark that overrides the type method is executed successfully.

# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
```
class A:
    def __init__(self,a):
        self.a=a
    def __lt__(self,other):
        return self.a<other.a
ob1=A(200)
ob2=A(30)
if(ob2<ob1):
    print("ob2 is less than ob1")
```
## Output
<img width="1027" height="167" alt="image" src="https://github.com/user-attachments/assets/2e40609a-d55b-41c1-97f9-a7dcb6028462" />


## Result
Thus the program that demonstrates operator overloading by overloading the less than (<) operator using a custom class is executed successfully

# # 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
```
class Beans: 
    def type(self):
        print("Vegetable")
    def color(self):
        print("Green")
     
class Mango():
    def type(self):
        print("Fruit")
    def color(self):
        print("Yellow")
obj_beans = Beans() 
obj_mango = Mango() 
for a in(obj_beans,obj_mango):
    a.type()
    a.color()
```
## Output
<img width="977" height="282" alt="image" src="https://github.com/user-attachments/assets/6f067cf6-9fb5-4181-b3ab-ef3cc9c0bc98" />


## Result
Thus the program To create two specific classes — Beans and Mango. Then, create a generic function that can accept any object and determine its type (Fruit or Vegetable) and color, using polymorphism is executed successfully
