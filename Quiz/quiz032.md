# Quiz 032

## Paper Solution

![quiz32](https://github.com/user-attachments/assets/261f68ea-222f-40b1-9ea0-b7e1dc202b1f)


## Code
```.py

class Human_Resources:
    def __init__(self,name:str,email:str, nationality:str, occupation:str):
        self.name=name
        self.email=email
        self.nationality=nationality
        self.occupation=occupation
    def get_email(self):
        return self.email
    def set_nationality(self,nationality_name):
        self.nationality=nationality_name
    def set_email(self,email):
        self.email=email
    def greet(self):
        print(f"Hello {self.name},you are working as {self.occupation} , your email is {self.email}, and  you are from {self.nationality}")

test=Human_Resources(name='Bob', email='bobsmith@gmail.com', nationality='American', occupation='Programmer')
test.greet()




```

## Proof of work
![image](https://github.com/user-attachments/assets/8bbe6289-03bd-407e-a751-825425db120f)

## UML Diagram
![image](https://github.com/user-attachments/assets/ca282f92-af5c-46c2-8aa4-e7ffb858f18a)



