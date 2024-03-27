
- SQL is a declarative language
	- you say what you want to do, not how 
	- not case sensitive

- DDL (Data Definition Language)
	- Created, Altering, and Removing database objects. 
	- Usually used by database administrators

- DML (Data Manipulation Language)
	- Retrieves and modify data
	- SELECT, UPDATE, INSERT, and DELETE
	- These are done on data within Tables 

- Select Statement 
	- Used to retrieve data from the database
	- Syntax
		- SELECT <columnName>
		- FROM <tableName>
	- SELECT studentFirstName, studentLastName, studentPhone
	- FROM student

- * WildCard
	- SELECT * 
	- This is a select all, meaning every row and every column

- Distinct Key Word
	- Sometimes a query returns multiple duplicate values
	- SELECT DISTINCT will return only one value instead

- Calculations
	- SELECT itemNumber, itemPrice, Quantity, itemPrice * itemQuanity
	- Operators include:
		- the standard ops (+,-,/)
		- Modulus
			- Returns the remainder in integer division 

- 