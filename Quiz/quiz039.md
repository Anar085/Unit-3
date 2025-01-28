# Quiz 039

## Python Code 
```.py

import sqlite3

db_name="my_database3.sql"

connection=sqlite3.connect(db_name)

cursor=connection.cursor()

haiku="""Code flows like a stream
Algorithms guide its way
In silence it solves"""
query_create= """CREATE TABLE if not exists haiku(
    id INTEGER PRIMARY KEY,
    word2 VARCHAR(150),
    length2 INTEGER
);

"""
cursor.execute(query_create)
connection.commit()

for word in haiku.split():
    new_word = f"INSERT INTO haiku (word2,length2) values ('{word}',{len(word)});"
    cursor.execute(new_word)
    connection.commit()



get_sum="SELECT AVG(length2) FROM haiku;"
result=cursor.execute(get_sum).fetchone()
print(result)
connection.close()


```


## Proof of work
![image](https://github.com/user-attachments/assets/22904f77-4beb-4a34-908f-bb3fdebf37c6)




