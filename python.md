# Python Note

## First class

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
