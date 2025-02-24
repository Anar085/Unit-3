# Quiz 046

## Python Code 
```.py
class Citizen:
    def __init__(self,name:str,city:str,status:str):
        self.name=name
        self.city=city
        self.status=status

    def getName(self)->str:
        return self.name
    def getCity(self)->str:
        return self.city
    def getStatus(self)->str:
        return self.status

class Employee(Citizen):
    def __init__(self,name:str,city:str,status:str,annual_salary:float):
        super().__init__(name,city,status)
        self.annual_salary=annual_salary

    def getAnnualSalary(self)->float:
        return self.annual_salary

class PartTimeEmployee(Employee):
    def __init__(self,name:str,city:str,status:str,annual_salary:float,fraction:float,union_member:bool):
        super().__init__(name,city,status,annual_salary)
        self.fraction=fraction
        self.union_member=union_member

    def getFraction(self)->float:
        return self.fraction
    def isUnionMember(self)->bool:
        return self.union_member

m=PartTimeEmployee("Bob Smith", "New York", "Employed", 90000, 0.5, True)
print(m.getName())
print(m.getAnnualSalary())
print(m.getFraction())
print(m.isUnionMember())

```


## Proof of work
![image](https://github.com/user-attachments/assets/71d2ab87-b5d0-4d73-b591-7dbb89cfea28)

## UML diagram
![image](https://github.com/user-attachments/assets/6cac9d9a-5268-413c-afe4-22c18dc9f922)





