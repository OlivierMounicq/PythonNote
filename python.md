# Python Note

## 1/ First class

```py
#Person class
class Person:
    def __init__(self, name, age) -> None:
         self.Name = name
         self.Age = age

    def ToString(self):
         return f'{self.Name}, {self.Age} years old'


p1 = Person("Olivier", 47)
print(p1.ToString())
```

## 2/ The class methods
- ```py__init__(self)``` : the constructor
- ```py__str__(self)``` : ToString() method

```py
  class Person:
    def __init__(self, name, age) -> None:
         self.Name = name
         self.Age = age

    def __str__(self) -> str:
         return f'{self.Name}, {self.Age} years old'

p1 = Person("Olivier", 47)
print(p1)
```

## 3/ The static class

```py
class MyMath:
    def Square(x) -> int:
        return x*x

MyMath.Square = staticmethod(MyMath.Square)

x = 2
print(f'The square of {x} is {MyMath.Square(x)}')
```

## 4/ The inheritance and the base class

```py
class Student(Person):
    def __init__(self, name, age, grade):
        Person.__init__(self, name, age)
        self.Grade = grade

    def __str__(self) -> str:
        return f'{super(Student, self).__str__()}  : {self.Grade}'
        

s1 = Student("Olivier", 47, "5th")
print(s1)
```

## 5/ The multiple inheritance

-> Method Resolution Order

```py
class A:
    def Method(a) -> str:
        return 'Class A -> Method'

class B:
    def Method(a) -> str:
        return 'Class B -> Method'
    
class C(B,A):
    pass

class D(A,B):
    pass

c = C()
print(c.Method())

d = D()
print(d.Method())
```
## 6/ Call another class from another class located in another file

```py
#File : Shape.py
class Circle:
    def __init__(self, radius) -> None:
        self.radius = radius

    def area(self):
        return 3.14 * (self.radius ** 2)    
```

```py
#File : main.py

from Shape import Circle

circle_instance = Circle(5)
print(circle_instance.area())
```
