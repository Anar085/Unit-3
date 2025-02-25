# Quiz 042

## Python Code 
```.py


import sqlite3
from secure_password import *

db_name="bitcoin_exchange (1).db"
connection=sqlite3.connect(db_name)
cursor=connection.cursor()
for_hash=""
get_query="""SELECT * from ledger 
"""
result=cursor.execute(get_query).fetchall()
names=["id","sender_id","receiver_id","amount"]
for lst in result:
    for i in range(len(lst)-1):
        for_hash+=f"{names[i]} {lst[i]},"
    for_hash=for_hash[:-1]
    print(for_hash)
    if check_hash2(input_str=for_hash,hash_str=lst[-1]):
        print("yes")
    else:
        print("no")
    for_hash=""


connection.close()



```


## Proof of work



![image](https://github.com/user-attachments/assets/9656e423-d227-43f0-8741-bf085e947756)

## ER Diagram


![image](https://github.com/user-attachments/assets/442ec837-8401-4d78-92f8-ac505e740ac7)


