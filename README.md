# sqlite3

Reviewing basic sqlite3 concepts to use SQL in python.

import sqlite3
conn = sqlite3.connect("my.db")
#1
cursor = conn.cursor()
q = 'select * from my_table'
cursor.execute(q)
results = cursor.fetchall()

#2
q = 'select * from my_table'
conn.execute(q).fetchall()

#3 using pandas
q = 'select * from my_table'
df = pd.read_sql_query(q, conn)
