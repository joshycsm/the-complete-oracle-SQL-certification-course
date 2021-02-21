# the-complete-oracle-SQL-certification-course

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
-
