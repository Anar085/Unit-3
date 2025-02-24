# Quiz 043

## Python Code 
```.py
class PalNum:
    def __init__(self,A:int,B:int):
        self.A=A
        self.B=B
    def get_pal_list(self):
        pal_list=[]
        for i in range(self.A,self.B+1):
            if str(i)==str(i)[::-1]:
                pal_list.append(i)
        return pal_list

m=PalNum(10, 99)
print(m.get_pal_list())


```


## Proof of work

![image](https://github.com/user-attachments/assets/0bf1441f-7565-4c4d-8dd3-7d9c7d76d3c8)



