# My SQL Progress Throughout the Summer

## Introduction
As summer comes to an end, I want to recount all the things that I've learned, specifically for a language called SQL. I started learning SQL in the beginning of the summer because, next to Excel, it is one of the most in-demand skills that are required to become a data scientist. I've been using this Udemy course called "The Complete SQL Bootcamp 2022: Go from Zero to Hero" that has helped me learn and practice the essential SQL concepts. I want to provide a quick summary, or cheat sheet, of what I've learned from the course so that you can refer to this post that could help you in the next query that you make!

Anyways, without furtherado, here is a recap of what I've learned about SQL:

---

## What is SQL?
SQL stands for Structured Query Language, and it is a language that allows a user to communicate with a database, which is a system that can store massive amounts of data.

---

## Fundamental Statements of SQL
### The SELECT Statement
The SELECT keyword is the bread and butter for writing queries. It is very simple yet powerful. You can do so many things with the SELECT statement, but I will save those for later. 

For right now, here's the syntax for selecting __one column__:
```tsql
SELECT column_name FROM table_name;
```

Syntax for selecting __multiple columns__:
```tsql
SELECT col_name1, col_name2 FROM table_name;
```

Syntax for selecting __everything__:
```tsql
SELECT * FROM table_name;
```

What a SELECT statement will do is return the column(s) that you want from a table. From here on out, things are going to be more complicated than this...

### The SELECT DISTINCT Statement
Now it's getting a bit more complicated. You can use the DISTINCT keyword combined with the SELECT statement to return all the __UNIQUE VALUES__ from a single column of a table. 

Syntax for SELECT DISTINCT:
```tsql
SELECT DISTINCT(col_name) FROM table_name;
```

Let's say that we have a __table called customers__ that stores who the customers from a certain store are:
| customer_id | customer_name |
| --- | --- |
| 1 | David |
| 2 | Mary |
| 3 | Sarah |
| 4 | David | 

If we want to find all of the __unique__ customer names, we can use a SELECT DISTINCT statement like so:
```tsql
SELECT DISTINCT(customer_name) FROM customers;
```

Running this query will return a list of __unique__ names:
| customer_name |
| --- |
| David |
| Mary |
| Sarah |

Note that this list only returns 3 names, whereas the original table had 4 names. This is because "David" appears in the table twice, and since SELECT DISTINCT only returns the __unique__ values, "David" is only returned once. 
