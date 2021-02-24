# the-complete-oracle-SQL-certification-course

### TO GET STARTED: [REQUEST A FREE WORKSPACE](https://apex.oracle.com/en/learn/getting-started/) AT ORACLE APEX https://apex.oracle.com/en/learn/getting-started/

## Section 1: Database Basics

### 1. Oracle Database Introduction & Basics of Tables

- 60% of Oracle SQL exam is about writing queries and getting them right. You can basically do anything in the Oracle database or any other database.
- Pass Microsoft SQL, PostgreSQL, MySQL.. slight differences in syntax but that's it.
- Disc is an easy way to represent a database. Set of hard drives essentially.
- Oracle is a software installed on a server or collection of servers even. Data is stored in the persistent disc (database).
- Instead of installing oracle database system onto our computer we are going to install Oracle cloud (i.e. Apex-website you can access database from and run query commands)
- Apex SQL command editor accessed using the browser. Master SQL practicing using the Apex tool.

### 2. Creating the Workspace in Oracle

- Apex: https://apex.oracle.com/en/
  - getting started
  - get a free workspace
- Practice is everything, you will not learn a thing if you don't practice.
- Don't be afraid to experiment with things and make mistakes.

### 3. IMPORTANT: Prepare the Sample Data

- emp, dept
- `SELECT * FROM dept;`
- `emp`
- Resources exist

### 4. How to Proceed in This Course

- Beginning to End (take once style)

## Section 2: Single Table Queries (Exercises & Solutions in the Lectures)

### 5. Oracle Exams and Certification Information

- This course prepares you to master SQL in the Oracle database environment. Oracle changes their certification paths all the time. But the core is the same. SQL.

- In this course we use Oracle 12c installed on the cloud. The SQL Language you'll be practicing is used in Oracle database versions 11G and 12C. Your job is to master Oracle SQL and you can only do that if you complete every single assignment in this course. Don't skip any opportunity to practice and struggle with the assignments. Once you have completed this course in addition to all of the assignments, you'll be ready to take the below exam!

- Oracle Database SQL (1Z0-071)

### 6. Retrieving Data Using the SELECT Clause

- All data is stored in tables and we need a way to query the data located in these table with the SELECT Clause.
- SQL language is NOT case senstive
- semicolon at end of every statement
- Let's deconstruct this SQL statement made up of keywords. Select key word. Reserved keyword in the SQL language. To retrive data from a table you'll need to call the select keyword. for `select * from emp;`
- at minimum need `SELECT <column> FROM <table>`;
- the above is a Query.
- just asking the database for some information we are looking for. that is essentially what a query is. select keyword is what makes this statement into a query.
- you can have `SELECT JOB, ENAME FROM EMP`;
- `*` Basically means give me everything you got. Whenver you want to do analysis of everything you have. You can get a quick view / snapshot what a table is all about.
- `distinct` is another keyword in the SQL language
- `select distinct job from emp;`

### 7. Using the WHERE Clause in a Query

- `select * from emp where job = 'MANAGER'`
-     select *
      from emp
      where job = 'MANAGER'
- When it comes to data SQL query needs to be very exact in these filter conditons.
- `AND` is another keyword in the SQL language. also `OR`
-     select *
      From emp
      where JOB = 'SALESMAN'
      and sal = 1600
      or comm = 500
- When we reference columns correctly but the data does not exist in a column then you will not recieve any hints or syntax error help. "no data found" will display
- we are using a tool called apex.
- oracle database can be installed for windows or linux when the proper hardware and software from oracle is available.
- on apex, a sql statement is sent to the oracle database. if it exists it executes the commands and returns us the data in the grid.
- What happens behind the scenes:
- select ...; select a column from a particular table
- from emp; in the from clause, it will find the particular table, emp in this case
- where sal = 3000; then it will go the where clause to look where the salary is 3000
- the interpreter will load the selected table and look for a column where a record is equivalent.
- oracle will return us a subset of the data we are looking for.
- make sure it is parsable / accurate.
- 1. The oracle interpreter sees the data we send it and makes sure the data we sent is parsable / accurate /correct
  2. The first thing it does is go to the from clause because this is the source of the data. This is what it interprets first. Does the table exist? if yes it loads it. otherwise not data found would be returned
  3. Then it moves onto the second statement which is the where clause and figures out which records does the user want to see? In this case it would be the records where salary = 3000. so it loads those records up and eliminates all the other records it doesn't need.
  4. finally, when it is done with the where clause, it goes to the select statement and filters out those particular columns / attributes we are trying to see.

### 8. Using Operators in the WHERE Clause

- Operators are used to compare one column with another or some data attribute.
- the first filter condition in a query is applied using the `where` clause and all of the other conditions after that are applied using the `and` clause
- `=` is the most common operator used with the `where` clause
- special operator in SQL is the `!` not operator
- so it will return everything other than etc.
- when you use incorrect logic, a query can still run but "no data found" will display.
- `SELECT * FROM EMP WHERE JOB = 'SALESMAN' AND SAL = 1500`
- the inequality operator can be used to filter queries.
-       SELECT * FROM EMP
        WHERE JOB != 'SALESMAN'
        AND SAL < 1500
- strings need to be wrapped in quotes
- you can use the inequlity operator to filter and query for a specific condition and return only that specific data.
- not managers salary greater than 2500 and work in dept number 20
- best practice, we always want the columns closer to the keyword.

### 9. Some Inspiration

- "fastest way to become a software developer video"
- 3 months oracle certification exam pass, 200 hours studying. 500 hours for oracle SQL certification exam more common.

### 10. Combining WHERE, AND & OR with Operators

-       SELECT * FROM EMP
        WHERE JOB != 'MANAGER'
        AND SAL > 2500
        AND DEPTNO = 20
-       SELECT *
        FROM EMP
        WHERE JOB = 'MANAGER'
- 1. SELECT \*; selecting which columns to looks at
  2. from emp; is our source. where are we getting the data from? the emp employee table
  3. where; filtering by some condition
- no data found can occur when you are not referencing the data strictly. You must have the exact string you're comparing against even tho SQL is not "case-senstive"
- `OR` is another keyword. This filter condition is useful for applying the criteria to each row of data where we might have two different conditions
- these conditions are applied for EVERY SINGLE RECORD.
- when the sql interpreter is ran, it is checking the record to meet the conditions exactly.
- filter criteria is checked on every single record in a particular table.
- SQL or any other programming disipline is about practice practice practice.
- all about the struggle and trying to work the problem out.
- The names of those employees that are not managers nor salesman and have a salary greater than or equal to 2000
- EVERY SINGLE RECORD IS CHECKED AGAINST EACH CONDITION
- Can result in misuse of OR / AND
- ASTRICK `*` IS GOOD to analyze data but when we have narrowed down to what we want to show then we can change the astrick to reflect the specific column we are actually interested in.
- puzzle: write a query that returns the names and hiring dates of those employees that work in dallas or chicago, slightly tricky because of requiremen of data analysis.
-       SELECT ENAME, HIREDATE
        FROM EMP, DEPT
        WHERE LOC = 'DALLAS'
        OR LOC = 'CHICAGO'
-       SELECT ENAME, HIREDATE
        FROM EMP
        WHERE DEPTNO = 20
        OR DEPTNO = 30
- we will soon get into how joins work and this will be a segue to that.

### 11. Query Filtering Continued BETWEEN, IN AND NULL

- 1. crucial to SQL syntax with single table SQL queries: `BETWEEN` and `IN` clause
- `IN` Clause allows us to not have as many conditions where we repeat the column name twice for a different condtion.

-       SELECT ENAME, HIREDATE
        FROM EMP
        WHERE DEPTNO IN (20, 30)
- `IN` Clause allows us to reduce the amount of SQL we need without using OR Clause when querying from a single column for multiple conditions.
-       SELECT ENAME, HIREDATE
        FROM EMP
        WHERE ENAME IN ('FORD', 'SMITH', 'ALLEN', 'WARD', 'MARTIN')
- In SQL, textual data requires quotations. numerical data does not. Single quotes not double quotes.
- `NOT IN` is another SQL keyword.
- Will return all names not listed in the condition.
- `BETWEEN` Operator another SQL keyword.
- In most database systems `BETWEEN` keyword can be used for textual, numeric and dates.
-       SELECT *
        FROM EMP
        WHERE HIREDATE BETWEEN '05/01/1981' AND '12/09/1982'
-       SELECT *
        FROM EMP
        WHERE SAL BETWEEN 1000 AND 2000
- `BETWEEN` is inclusive to include the conditional range.
- `NOT BETWEEN` another keyword. Negates the `BETWEEN` condition
- to identify empty cells: null means no particular data from a given record. Can return empty cell with `NULL` keyword. Also can use `IS NOT NULL`
-       SELECT *
        FROM EMP
        WHERE COMM IS NULL
        AND SAL BETWEEN 1100 AND 5000
        AND SAL NOT IN 3000

### 12. What Will Make you Grow as a Software Developer

- Perspective: learn databases, learn SQL first. Companies are gonna need database developers. Afterwards, learn corporate culter and development lingo / lifecycle.
- gonna need data analyst, report builders, understand how software development life cycles work.
- No one can teach you to code.
- The only way to learn to code is doing it on your own. Code on your own.
- The real learning is done on those weekend nights when you can't figure it out yourself and a light bulb goes off a day or week later. That's what it's all about to learn and become a software developer.
-

### 13. Query Filtering Condtions and Operator Precedence TRICKY

- null cannot equal to null. that's why we have `is null` keyword.
-       SELECT *
        FROM EMP
        WHERE COMM IS NULL
        AND SAL > 1100 AND SAL < 5000
        AND SAL <> 3000
        OR COMM = 0
- We always want to tag `or` at the end.
- parenthesis cause conditions to be evaluated together.
- When you have multiple condtions to be evalued together wrap them in parenthesis.
-       SELECT *
        FROM EMP
        WHERE (COMM IS NULL OR COMM = 0)
        AND SAL > 1100 AND SAL < 5000
        AND SAL != 1500
- wrapped in parenthesis will be evaluated first and conditions will be checked first. then other conditions will be evaluated after those in parenthesis.
-       SELECT *
        FROM EMP
        WHERE JOB = 'SALESMAN'
        AND (COMM = 300
        OR COMM > 1000)
- another operator keyword is `like`
- Benefit of like is you don't have to return the entire exact word. it can give you all the data that has a specific pattern `S%` `%` is known as a wild card and will match any other characters that follow the compulsory item which is S.
-       SELECT *
        FROM EMP
        WHERE JOB LIKE 'SA%'
        OR JOB LIKE '%ER'
- SECTION 14 WILL TALK ABOUT ALIASES AND HOW TO CHANGE THE WAY DATA LOOKS IN THE OUTPUT

### 14. Ordering, Concatenating & Aliasing Query Results

- how to use aliases for displaying more meaningful column names rather than the table's defaults.
- learn how to display the results of a query in a more customizable format using something called concatenation
- ordering data based on certain attributes of the table
- SQL standard is the `AS` keyword.
- Concatenation is the combining of two attributes together into a sentence.
- special operator that's used to concatenate strings together called pipes `||`
-       SELECT ENAME || ' makes $' || SAL || ' per month'
        AS "MONTHLY SALARY REPORT FOR EMPLOYEES"
        FROM EMP
        WHERE JOB = 'MANAGER'
- `ORDER BY` clause is used to sort the data based on a particular column.
- THE entire record gets placed in the proper position from top to bottom, not just the single column.
- `DESC` keyword will sort in descending order.
-       SELECT *
        FROM EMP
        ORDER BY DEPT, SAL DESC
- `ASC` smallest to largest; IS DONE BY DEFAULT
- ORDER BY AFTER SELECT, FROM , WHERE.
- It is one of the last clauses processed by the database query engine.
- WILL TALK MORE ABOUT ORDERING AND PRACTICE PROBLEMS NEXT.

### 15. Assingment 1: Practice with Single Table Queries

1. Write a query that retrieves suppliers that work in either Georgia or California.

-       SELECT *
        FROM <TABLE> suppliers
        WHERE STATE IN ('Georgia','California')

2. Write a query that retrieves suppliers with the characters "wo" and the character "I" or "i" in their name.

-       SELECT *
        FROM suppliers
        WHERE supplier_name like '%wo%'
        and (supplier_name like '%I%'
        or supplier_name like '%i%')

3. Write a query that retrieves suppliers on which a minimum of 37,000 and a maximum of 80,000 was spent.

-       SELECT *
        FROM suppliers
        WHERE total_spent between 37,000 and 80,000

4. Write a query that returns the supplier names and the state in which they operate meeting the following conditions:

belong in the state Georgia or Alaska

the supplier id is 100 or greater than 600

the amount spent is less than 100,000 or the amount spent is 220,000

-       SELECT supplier_name, state
        FROM suppliers
        where (supplier_id > 600 or supplier_id = 100)
        AND state in ('Georgia', 'Alaska')
        AND (total_spent < 100000 or total_spent = 220000)

5. TRUE or FALSE Question: FALSE

The keywords such as SELECT and WHERE must always be capital in the SQL Query.

6. TRUE or FALSE Question: FALSE

The database works on first processing the filtering conditions and then processes the FROM condition.

7. TRUE or FALSE Question: TRUE

Having just the filter condition shown below in a SQL query will return all of the records from the table.

WHERE 1 = 1

8. TRUE or FALSE question: TRUE

NULL can not be compared using an equal sign.

9. TRUE or FALSE question: FALSE

The ORDER BY clause is processed before the FROM clause in a SQL statement and it's used to sort the columns in an ascending or descending fashion.

<!-- Oracle and Structured Query Language (SQL)

Identify the connection between an ERD and a Relational Database
Explain the relationship between a database and SQL
Describe the purpose of DDL
Describe the purpose of DML
Build a SELECT statement to retrieve data from an Oracle Database table
Restricting and Sorting Data

Use the ORDER BY clause to sort SQL query results
Limit the rows that are retrieved by a query
Use ampersand substitution to restrict and sort output at runtime
Use SQL row limiting clause
Using Single-Row Functions to Customize Output

Use various types of functions available in SQL
Use character, number, and date and analytical (PERCENTILE_CONT, STDDEV, LAG, LEAD) functions in SELECT statements
Using Conversion Functions and Conditional Expressions

Describe various types of conversion functions that are available in SQL
Use the TO_CHAR, TO_NUMBER, and TO_DATE conversion functions
Apply general functions and conditional expressions in a SELECT statement
Reporting Aggregated Data Using the Group Functions

Describe the use of group functions
Group data by using the GROUP BY clause
Include or exclude grouped rows by using the HAVING clause
Displaying Data from Multiple Tables

Describe the different types of joins and their features
Use SELECT statements to access data from more than one table using equijoins and nonequijoins
Join a table to itself by using a self-join
View data that generally does not meet a join condition by using outer joins
Using Subqueries to Solve Queries

Define subqueries
Describe the types of problems subqueries can solve
Describe the types of subqueries
Query data using correlated subqueries
Update and delete rows using correlated subqueries
Use the EXISTS and NOT EXISTS operators
Use the WITH clause
Use single-row and multiple-row subqueries
Using the Set Operators

Describe set operators
Use a set operator to combine multiple queries into a single query
Control the order of rows returned
Manipulating Data

Truncate data
Insert rows into a table
Update rows in a table
Delete rows from a table
Control transactions
Using DDL Statements to Create and Manage Tables

Describe data types that are available for columns
Create a simple table
Create constraints for tables
Drop columns and set column UNUSED
Create and use external tables
Managing Objects with Data Dictionary Views

Query various data dictionary views
Controlling User Access

Differentiate system privileges from object privileges
Grant privileges on tables and on a user
Distinguish between privileges and roles
Managing Schema Objects

Describe how schema objects work
Create simple and complex views with visible/invisible columns
Create, maintain and use sequences
Create and maintain indexes including invisible indexes and multiple indexes on the same columns
Perform flashback operations
Manipulating Large Data Sets

Describe the features of multitable INSERTs
Merge rows in a table
-->
