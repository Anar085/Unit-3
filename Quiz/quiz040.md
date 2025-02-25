# Quiz 040

## Python Code 
```.py
import sqlite3

from docutils.nodes import problematic

from secure_password import *

db_name="smallCase.db"
connection=sqlite3.connect(db_name)
cursor=connection.cursor()
for_hash=""
problematic_customers=[]
for id in range(1,21):
    get_query=f"""SELECT * from transactions where account_id={id}"""
    result=cursor.execute(get_query).fetchall()
    customer_balance1=0
    for element in result:
        if element[1]=="deposit":
            customer_balance1+=int(element[2])
        if element[1]=="withdraw":
            customer_balance1-=int(element[2])
    get_query2=f"""SELECT * from accounts where account_id={id}"""
    result2=cursor.execute(get_query2).fetchone()
    customer_balance2=int(result2[2])
    if customer_balance1!=customer_balance2:
        problematic_customers.append(id)

print(f"Here are the ids of problematic_customers: {problematic_customers}")
connection.close()



```


## Proof of work

![image](https://github.com/user-attachments/assets/9c9e014d-ba97-4cb6-a73a-f57e485eada8)




