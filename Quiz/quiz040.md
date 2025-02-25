# Quiz 040
## ER diagram

![image](https://github.com/user-attachments/assets/9987fafb-d3b7-4315-8652-a7805b8347ed)




## Python Code 
```.py
import sqlite3

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
print(f"Here are of problematic customers:")
for customer_id in problematic_customers:
    get_user_query=f"""SELECT first_name,last_name from customers where customer_id={customer_id}"""
    result3=cursor.execute(get_user_query).fetchone()
    customer=f"{result3[0]} {result3[1]}"
    print(customer)

connection.close()





```


## Proof of work


![image](https://github.com/user-attachments/assets/11ff13a2-585b-4e01-b279-0f71f646e30b)



