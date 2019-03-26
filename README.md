# sqlite3

Reviewing basic sqlite3 concepts to use SQL in python.<br />
<br />
import sqlite3 <br/>
conn = sqlite3.connect("my.db") <br />
##1<br />
cursor = conn.cursor()<br />
q = 'select * from my_table'<br />
cursor.execute(q)<br />
results = cursor.fetchall()<br />
<br />
##2<br />
q = 'select * from my_table'<br />
conn.execute(q).fetchall()<br />
<br />
##3 using pandas<br />
q = 'select * from my_table'<br />
df = pd.read_sql_query(q, conn)<br />
