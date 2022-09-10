# My SQL Progress Throughout the Summer (Part 2)

## Introduction
Welcome to Part 2 of this blog post series! This will be the final part, but I will be posting other data science related content about once a week, so stay tuned! Also, if you haven't already, please check out the [Part 1 of my SQL progress in the summer](https://dylans0ng.github.io/2022/09/04/sql-progress-part-1.html). 

Anyways, without furtherado, let's dive into the main topic of this post: creating and modifying tables in SQL! Keep in mind that this post is a brief overview, NOT a comprehensive guide. 

---

## First... the basics: Data Types
If you want to make tables in SQL, you must understand the different data types that you can have. __Data types basically describe what kind of data the variable is__. For example, if you have a variable that stores a value of 5, then the __data type__ is "integer" because 5 is a number. If you have previous programming knowledge in a different language, this will make a lot of sense. 

Here's a list of some data types:

- **Boolean**: True or false

- **Character**: Char, varchar, and text

- **Numeric**: Integer and floating-point number

- **Temporal**: Date, time, timestamp, and interval

- **Array**: Stores an array of strings, numbers, etc

Tip: when you create a table, think about **what data type you want to use** to store the data. For example, if you want to store a column of phone numbers in a table, you should use a **text-based data type** because you can't really do arithmetic operations on a phone number. **Remember that not all numbers should have numeric data types**.

## Primary & Foreign Keys 

What is a **primary key**?

- A **primary key** is a column used to identify a row **uniquely in a table**. There can **only be one** primary key in a table.

- Useful for **joining** tables together

- Let's look at an example table:

| customer_id | name | age |
| --- | --- | --- |
| 1 | David | 24 |
| 2 | Mary | 36 |
| 3 | Sarah | 19 |
| 4 | David | 50 |

- In this case, the "customer_id" column holds a **unique value** for each customer in the table. Thus, "customer_id" is a **primary key**.

Now, let's transition over to **foreign keys**. 

- A **foreign key** is defined in a table that references to the primary key in **another table**. You can have **multiple** foreign keys in a table.
