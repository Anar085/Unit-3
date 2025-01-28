# Quiz 033

## Paper Solution

![quiz33](https://github.com/user-attachments/assets/298a7495-bb91-4e1d-a4d1-5891f4f9ec3e)


## Code
```.py

class CompoundInterest:
    def __init__(self,principal:float,rate:float):
        self.principal=principal
        self.rate=rate
    def calculate(self,years:int)->float:
        return self.principal*(1+self.rate)**years

test=CompoundInterest(principal=1000, rate=0.05)
print(test.calculate(years=2))



```

## Proof of work


![image](https://github.com/user-attachments/assets/9965ca92-e916-4836-b42a-f3c1d6a00fb3)

