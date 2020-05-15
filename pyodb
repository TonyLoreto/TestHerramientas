pip install pyodbc

def read(conn):
  print("Read")
  cursor = conn.cursor()
  cursor.execute("select * from db")
  for row in cursor:
    print(f'row = {row}')
  print()

def create(conn):
  print("Create")
  cursor = conn.cursor()
  cursor.execute(
    'insert into db(a,b) values(?,?);',
    (0000,'asdf')
  )
  conn.commit()
  read(conn)
 
def update(conn):
  print("Update")
  cursor = conn.cursor()
  cursor.execute(
    'update db set b = ? where a = ?;',
    (1111,'qwer')
  )
  conn.commit()
  read(conn)
  
def delete(conn):
  print("Delete")
  cursor = conn.cursor()
  cursor.execute(
    'delete from db where a > ?'
  )
  conn.commit()
  read(conn)  

import pyodbc
conn=pyodbc.connect(
  "Driver={};"
  "Server=;"
  "Database=;"
  "Trusted_Connection=yes;"
  )
  
  
  
  read(conn)
  create(conn)
  update(conn)
  delete(conn)
  
  conn.close()
