# Quiz 034

## Paper Solution
![quiz34](https://github.com/user-attachments/assets/77f97e46-f926-4a79-8e6c-f51a31402f8a)



## Code
```.py

class Flight:
    def __init__(self,number:str,departure:str,arrival:str, distance:int, airplane:str):
        self.number=number
        self.departure=departure
        self.arrival=arrival
        self.distance=distance
        self.airplane = airplane
    def info(self):
        print(f"Flight Number: {self.number}\n"
              f"Departure: {self.departure}\n"
              f"Arrival: {self.arrival}\n"
              f"Distance: {self.distance} km\n"
              f"Airplane: {self.airplane}")
test=Flight(number="AZH085", departure="Baku", arrival="Istanbul", distance=1500, airplane="Airbus A340")
test.info()

```

## Proof of work
![image](https://github.com/user-attachments/assets/d1143790-3523-40bc-bc4e-408fc1f57e19)



