Title: PostgreSQL Index Performance Exercise with EXPLAIN and ANALYZE

Objective:To understand the impact of indexes on query performance in PostgreSQL using the EXPLAIN and ANALYZE commands.

Exercise:Consider containing a table named "employees" with the following structure:

CREATE TABLE employees ( employee\_id SERIAL PRIMARY KEY, first\_name VARCHAR(50), last\_name VARCHAR(50), department VARCHAR(50), salary INTEGER);

You've populated the "employees" table with a substantial amount of data. Now, let's create an index on the "department" column:CREATE INDEX department\_index ON employees (department);You've been provided with two sample SQL queries:

Query 1: Retrieve all employees from the "Sales" department with a salary greater than 50000.

EXPLAIN ANALYZESELECT \* FROM employees WHERE department = 'Sales' AND salary > 50000;

Query 2: Retrieve all employees from the "Marketing" department with a salary greater than 60000.EXPLAIN ANALYZESELECT \* FROM employees WHERE department = 'Marketing' AND salary > 60000;Tasks:

1.  Execute Query 1 and Query 2 without any indexes and record their execution times.
    
2.  Create the index "department\_index" on the "department" column.
    
3.  Execute Query 1 and Query 2 again with the newly created index and record their execution times.
    
4.  Analyze and compare the execution plans and times before and after creating the index.
    
5.  Discuss the observations and conclusions regarding the impact of the index on query performance.
