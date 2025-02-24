# Quiz 047

## Python Code 
```.py
class CalorieCount:
    def __init__(self,daily_limit:int):
        self.daily_limit=daily_limit
        self.daily_intake=0
        self.protein=0
        self.carbs=0
        self.fat=0

    def addMeal(self,cal:int,pro:int,car:int,fat:int):
        self.daily_intake+=cal
        self.protein+=pro
        self.carbs+=car
        self.fat+=fat
    def getProteinPercentage(self) -> float:
        if self.daily_intake==0:
            return 0
        return (4*self.protein)/self.daily_intake
    def onTrack(self)->bool:
        if self.daily_intake<=self.daily_limit:
            return True
        else:
            return False
sunday=CalorieCount(1500)
sunday.addMeal(716, 38, 38, 45)
sunday.addMeal(230, 16, 8, 16)
sunday.addMeal(568, 38, 50, 24)
print(sunday.onTrack())
print(f"{sunday.getProteinPercentage():.2f}")
```


## Proof of work
![image](https://github.com/user-attachments/assets/437601c0-dde7-444d-a4d0-515054f564ec)

## UML diagram
![image](https://github.com/user-attachments/assets/64ce750f-ec2a-4943-8cf5-5868c59d4fa0)





