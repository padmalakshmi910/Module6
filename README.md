## Python OOP: Abstract Class & Method Exampl
## AIM
To create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle.

## ALGORITHM
```
Import ABC module:

1.Use from abc import ABC, abstractmethod to define abstract classes and methods.
Create Abstract Class Shape:

2.Define an abstract method calculate_area() with @abstractmethod.
Create Subclass Rectangle:

3.Set default values for length and breadth.
Override calculate_area() to compute the rectangle area.
Create Subclass Circle:

4.Set default value for radius.
Override calculate_area() to compute the circle area.
Create Objects & Call Methods:

5.Instantiate Rectangle and Circle.
Call their calculate_area() methods.
```
## Program
```
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius
radius = float(input("Enter radius: "))
c = Circle(radius)
print("Area of Circle =", c.area())
```
## Output
<img width="1280" height="711" alt="Screenshot 2026-06-01 190736" src="https://github.com/user-attachments/assets/699b178c-5948-41e8-9de5-0ff6a0ac78e9" />

## Result
Thus, the program has been executed successfully.

## Python OOP: Encapsulation with Private Members
## AIM
To implement Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth.

## ALGORITHM
```
1.Define the Class:

2.Create a class Rectangle with two private attributes: __length and __breadth.
Initialize Variables:

3.Use the __init__() constructor to set initial values for __length and __breadth.
Print Values:

4.Display the private variables from within the class to demonstrate access.
Instantiate the Object:

5.Create an object of the Rectangle class to trigger the constructor.
```
## Program
```
class Rectangle:
    def __init__(self, length, breadth):
        self.__length = length
        self.__breadth = breadth
        print("Length:", self.__length)
        print("Breadth:", self.__breadth)

rect = Rectangle(10, 5)
```
## Output
<img width="1333" height="339" alt="Screenshot 2026-06-01 191156" src="https://github.com/user-attachments/assets/762468cd-0924-4d62-a8dc-d7c8a4e3d397" />

## Result
Thus, the program has been executed successfully.
## Method Overriding-Fish and Shark Class Inheritance in Python
## AIM:
To write a Python program that demonstrates class inheritance by creating a parent class Fish with a method type, and a child class Shark that overrides the type method.

## ALGORITHM:
Define the Fish class with a method named type() that prints "fish".
Define the Shark class as a subclass of Fish, and override the type() method to print "shark".
Create an instance of the Fish class named obj_goldfish.
Create an instance of the Shark class named obj_hammerhead.
Use a for loop to iterate over both objects.
Within the loop, call the type() method using the loop variable.
Output will demonstrate method overriding: printing "fish" and "shark" accordingly.
## PROGRAM:
```
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
    def type(self):
        print("shark")

obj_goldfish = Fish()
obj_hammerhead = Shark()

for fish in (obj_goldfish, obj_hammerhead):
    fish.type()
```
## OUTPUT
<img width="1230" height="465" alt="Screenshot 2026-06-01 191532" src="https://github.com/user-attachments/assets/c12da222-4a98-4234-9110-0f6b0db92a1d" />

## RESULT
Thus, the program has been executed successfully.

## Python OOP: Operator Overloading (Less Than <)
## AIM
To write a Python program that demonstrates operator overloading by overloading the less than (<) operator using a custom class.

## ALGORITHM
```
Create Class A:

Define the __init__() method to initialize the object with a value a.
Overload the < Operator:

Define the __lt__() method with logic:
If self.a < o.a, return "ob1 is less than ob2"
Else, return "ob2 is less than ob1"
Create Objects:

Instantiate two objects ob1 and ob2 with values.
Use < Operator:

Use print(ob1 < ob2) to trigger the overloaded behavior.
```
## Program
```
class A:
    def __init__(self, a):
        self.a = a

    def __lt__(self, other):
        if self.a < other.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"

ob1 = A(10)
ob2 = A(20)

print(ob1 < ob2)
```
## Output
<img width="1271" height="491" alt="Screenshot 2026-06-01 191723" src="https://github.com/user-attachments/assets/cfeb4ff5-a6ec-404f-acb5-b2da881ba46c" />

## Result
Thus, the program has been executed successfully.

## Python OOP: Polymorphism with Classes
## AIM
To create two specific classes — Beans and Mango. Then, create a generic function that can accept any object and determine its type (Fruit or Vegetable) and color, using polymorphism.

## ALGORITHM
```
Create Class Beans:

Define type() method that prints "Vegetable".
Define color() method that prints "Green".
Create Class Mango:

Define type() method that prints "Fruit".
Define color() method that prints "Yellow".
Define Generic Function func(obj):

Call obj.type() and obj.color() — this works with both Beans and Mango objects, showcasing polymorphism.
Create Objects:

Instantiate Beans and Mango.
Pass them to func() and execute the program.
```
## Program
```
class Beans:
    def type(self):
        print("Vegetable")
    def color(self):
        print("Green")

class Mango:
    def type(self):
        print("Fruit")
    def color(self):
        print("Yellow")

def func(obj):
    obj.type()
    obj.color()

b = Beans()
m = Mango()

func(b)
func(m)

```
## Output
<img width="1244" height="698" alt="Screenshot 2026-06-01 191901" src="https://github.com/user-attachments/assets/96f796bc-7a6c-4537-af7e-994dee87c6c4" />

# Result
Thus, the program has been executed successfully.
