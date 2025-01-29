# Quiz 035

## Paper Solution
![quiz35](https://github.com/user-attachments/assets/ffa4717d-b91a-434a-b699-ef194ae174a2)



## Code
```.py
class Person:
    def __init__(self,name:str,age:int):
        self.name=name
        self.age=age
    def get_name(self):
        return self.name
    def get_age(self):
        return self.age
class Student(Person):
    def __init__(self,name:str,age:int,grade:int):
        super().__init__(name,age)
        self.grade=grade
    def get_grade(self):
        return self.grade

test=Student(name='Bob',age=10,grade=9)
print(test.get_grade())


```

## Proof of work
![image](https://github.com/user-attachments/assets/06c1d1c9-6828-4e37-b920-157360673cd8)

## UML Diagram
![image](https://github.com/user-attachments/assets/9d94502e-d21d-477b-ae6d-ef5d21f32899)


