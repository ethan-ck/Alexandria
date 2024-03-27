
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
			- 3/10 = 3r1 
	- Follows PEMDAS

- Sorting
	- Sort results using the keywords ORDER BY
		- SELECT *
		- FROM Session
		- ORDER BY SessionDate
	- ORDER BY does ascending by default

- Aliasing
	- Sometimes it is useful to alias a column name to make it more readable
	- SELECT studentLastName AS [lastname], StudentFirstName AS [firstname]

- Where clause
	- The WHERE clause limits the rows returned in a query
	- You use the WHERE clause to specify the criteria by which the rows will eb filtere
	- SELET LastName,FirstName, Phone, City
	- FROM Customer
	- WHERE City = "Seattle"

- Other Criteria
	- Relational operators
	- =, <, >,=<, and <> (not equal to)

- Like
	- the LIKE keyword used in a WHERE operator with a wildcard allows you to search for patterns in character-based fields
	- The following returns all items whose name starts with "T"
		- SELECT ItemName, ItemPrice
		- FROM inventory
		- WHERE ItemName LIKE "T%"
	- Must use % as a 

- Between
	- BETWEEN keyword used in criteria to return a range of values
	- BETWEEN is inclusive of its needs
	- SElect TutorKey, SessionDate, StudentKey
	- FROM Session
	- WHERE SessionDate BETWEEN (Date here) AND (date here)

- AND, OR, NOT (Logical Boolean Operators)
	- AND is specific
	- OR is more
	- NOT excludes 

- NULL 
	- Special, They are NOT a value and CANNOT be compared
	- Use the IS keyword in criteria 
	- WHERE StudentKey IS NULL
	- WHERE StudentKey IS NOT NULL

- Functions
	- Functions in SQL has the same basic syntax as python
	- Main()

- Scalar Functions operate on a single row at a time
	- GETDATE()
	- MONTH()
	- YEAR()

- Aggregate Function operates on multiple rows at a time
	- COUNT()
	- SUM()
	- AVG()
	- MAX()
	- MIN()

- HAVING
	- The HAVING keyword is used when tehre is an aggregate funciton in the criteria of a query
	- SELECT TutorKey, COUNT(SessionTimeKey) AS [Total Sessions]
	- FROM Session
	- GROUP BY TutorKey
	- HAVING Count(SessionTimeKey) (Greater than or equal to symbol) 4

- Joins
	- In database design and normalization, the data is broken into several discrete tables
	- Joins are the mechanism for recombing the data into one reuslt 
	- Three kinds of joins:
		- Inner Joins 
		- Equi Joins 
		- Outer Joins 

- Inner Join 
	- Inner joins return related records from each of the tables joined
	- SELECT column1 AND column2
	- FROM table1
	- INNER JOIN table2
	- ON table1.column1.column2

- Equi Joins
	- Presents an alternative way to perform inner joins. Some older RDMSs only support this alternative form. 

- OUTER JOIN 
	- Outer join return records that are not matched, joins records from first table and related records from second table
	- SELECT Column1, column2
	- FROM table1
	- LEFT OUTER JOIN table2
	- ON table1.Column>=table2.column

-  Begin the comment with a slash and an asterisk (/*). Proceed with the text of the comment. This text can span multiple lines. End the comment with an asterisk and a slash (*/).
	- /* Begin comment like this, end comment like this */

- 