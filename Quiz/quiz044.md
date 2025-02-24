# Quiz 044

## Python Code 
```.py
class rainDrops:
    def __init__(self,n:int):
        self.n=n
    def pour(self):
        out=''
        if self.n%3==0:
            out+='Pling'
        if self.n%5==0:
            out+='Plang'
        if self.n%7==0:
            out+='Plong'
        if out=='':
            out=str(self.n)
        return out
m=rainDrops(n=28)
print(m.pour())
```


## Proof of work

![image](https://github.com/user-attachments/assets/be24475a-b116-4065-8f29-cb8b734610c7)



