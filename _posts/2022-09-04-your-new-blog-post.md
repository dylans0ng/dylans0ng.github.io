# My SQL Progress Throughout the Summer (Part 1) 

## Table of Contents
* [Introduction](#introduction)
* [The SELECT Statement](#the-select-statement)
* [SELECT DISTINCT](#select-distinct)
* [COUNT](#count)
* [SELECT WHERE](#select-where)
* [GROUP BY](#group-by)
* [Conclusion](#conclusion)

## Introduction
As summer comes to an end, I want to recount all the things that I've learned, specifically for a language called SQL, which allows a user to communicate with a database. I started learning SQL in the beginning of the summer because, next to Excel, it is one of the most in-demand skills that are required to become a data scientist. I've been using this Udemy course called "The Complete SQL Bootcamp 2022: Go from Zero to Hero" that has helped me learn and practice the essential SQL concepts. I want to provide a quick summary, or cheat sheet, of some important keywords that you can use for the SELECT statement! This is a Part 1 of my post, and I will create a Part 2 in the future covering creating and modifying a table, so stay tuned for that!

Anyways, without furtherado, here is a recap of a few important things about the SELECT statement:

---

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

---

### SELECT DISTINCT
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

---

### COUNT 
The COUNT keyword does just what it sounds. It counts the rows in the table. In more complex terms, it returns the number of input rows that match a specific condition of a query.

You use COUNT with the SELECT statement. Here's what the syntax looks like:
```tsql
SELECT COUNT(*) FROM table_name;
```

Let's use the customers table from the previous example again:
| customer_id | customer_name |
| --- | --- |
| 1 | David |
| 2 | Mary |
| 3 | Sarah |
| 4 | David | 

To use the COUNT keyword, we can do this in our query:
```tsql
SELECT COUNT(*) FROM customers;
```
What this code does is return the number of rows in the table. It's that simple. 

Now you can make it more complex by using COUNT and DISTINCT together. Doing this will __count__ the number of __unique values__ in the table.

For example,
```tsql
SELECT COUNT(DISTINCT(customer_name)) FROM customers;
```
will return 3 because there are 3 __unique values__ in the column called "customer_name".

In most cases, using the COUNT keyword won't be this easy. You will often use a WHERE statement to specify the condition for the count of number of rows. 

---

### SELECT WHERE
The SELECT WHERE statement is probably the most important out of all the other keywords that I talk about in this post. 

What the WHERE statement does is that it allows you to **specify the conditions for the rows in the table to be returned**. If you have some experience in a programming lanaguage such as Python, then **think of WHERE as an "if" statement**. 

General syntax:
```tsql 
SELECT column_name
FROM table_name
WHERE condition(s);
```

Let's use an example to make this more clear, using a table called "customer" (similar to the previous example):
| customer_id | customer_name | customer_age |
| --- | --- | --- |
| 1 | David | 25 |
| 2 | Mary | 40 |
| 3 | Sarah | 60 |
| 4 | David | 65 |

Let's say we say something like this:
```tsql
SELECT customer_name
FROM customer
WHERE customer_age >= 60;
```

This query will return two names: "Sarah" and "David". This is because the customers with a name of Sarah and David have an age at least 60, **meaning that they meet the condition in the WHERE statement**. 

Another cool thing we can do is use something called the **AND keyword**. This basically allows you to **combine multiple conditions** in a single WHERE statement. Keep in mind that if you use **AND**, then all of the conditions must be true for the rows to be returned.

Using the same example above, if we say
```tsql
SELECT customer_name
FROM customer
WHERE customer_age < 63 AND customer_age > 35;
```
the query will return "Mary" and "Sarah". This is because those people are the only ones that meet **BOTH** of the age requirements listed in the WHERE statement.

---

### GROUP BY 
In order to use the GROUP BY keyword, you must understand what **aggregation functions** are.

**Aggregation functions** take multiple inputs from a whole column and return a single result. Examples include AVG(), COUNT(), MAX(), MIN(), SUM().

Let's have a sample table called "players" to show how **aggregation functions** work:
| player_id | player_height_inches | player_location |
| --- | --- | --- |
| 1 | 70 | Seattle, Washington |
| 2 | 75 | San Francisco, California |
| 3 | 80 | Toronto, Ontario |
| 4 | 67 | Boston, Massachusetts |

Doing 
```tsql
SELECT AVG(player_height_inches)
FROM players
```
will return 73 because the mean was returned.

Ok, now back to the **GROUP BY**. 

Basically, **GROUP BY** groups the values in a CATEGORICAL column and perfoms an aggregation function on a QUANTITATIVE column and returns the aggregated quantitative values for each value in the categorical column.

If that sounded confusing, then consider this table called "players": 
| player_id | player_height_inches | player_location |
| --- | --- | --- |
| 1 | 70 | Seattle, Washington |
| 2 | 75 | San Francisco, California |
| 3 | 80 | Toronto, Ontario |
| 4 | 67 | Boston, Massachusetts |
| 5 | 65 | Seattle, Washington |
| 6 | 71 | Seattle, Washington |
| 7 | 74 | Toronto, Ontario |
| 8 | 66 | San Francisco, California |
| 9 | 69 | Toronto, Ontario | 
| 10 | 73 | Boston, Massachusetts |

If we wanted to find the **maximum height** for each player from a specific location, then we can use **GROUP BY**. Here's how we do it:
```tsql
SELECT player_location, MAX(player_height_inches)
FROM players
GROUP BY player_location;
```

This will return something that looks like this:
| player_location | player_height_inches |
| --- | --- |
| Seattle, Washington | 71|
| San Francisco, California | 75 |
| Toronto, Ontario | 80 |
| Boston, Massachusetts | 73 |

Notice that in the query, the categorical column that is NOT being aggregated "player_location" is the one that is being grouped. NEVER group by the quantitative column, which in this case is "player_height_inches".

Also, the **GROUP BY keyword** should come right after the FROM statement. While the query above looks quite simple, it can get pretty complicated once add WHERE statements and other SQL commands.

--- 

## Conclusion
I hope you've learned some of the basics of SQL in this post! All of these things are NOT a comprehensive list of the whole language. I only covered a glimpse of SQL, and to dive deeper, you can view a Postgres documentation at https://www.postgresql.org/docs/15/index.html. If you want, please comment down below what SQL commands you use the most often in your job.

Thank you for reading!
