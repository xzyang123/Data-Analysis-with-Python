## Accessing databases using python

* Using DB-API calls

## Concepts of the Python DB API

**Connection Objects**

*connect to database and manage the transactions*
* Database connections
* Manage transactions

**Cursor Objects**

*Used to run queries*
* Databae Queries

## Connection Methods

* cursor() 

*returns a new cursor object using the connection*

* commit()

*commit any pending transaction to the database*

* rollback()

*casuses the DB to roll back to the start of any pending transaction*

* close()

*close the DB connection*

## Writing code using DB-API

```python
from dbmodule import connect

#Create connection object
connection = connect('databasename', 'username', 'pswd')

#cursor is used to run queries and fetch results
cursor = connection.cursor()

#Run queries
cursor.execute('select * from mytable')

#Free resources
cursor.close()
connection.close()
```

