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


