# My SQL Progress Throughout the Summer (Part 2)

## Table of Contents
* [Introduction](#introduction)
* [First... the basics: Data Types](#first-the-basics-data-types)
* [Primary & Foreign Keys](#primary-and-foreign-keys)
* [Constraints](#constraints)
* [CREATE Table](#create-table)
* [INSERT](#insert)
* [UPDATE](#update)
* [DELETE](#delete)
* [Conclusion](#conclusion)

## Introduction
Welcome to Part 2 of this blog post series! This will be the final part, but I will be posting other data science related content about once a week, so stay tuned! Also, if you haven't already, please check out the [Part 1 of my SQL progress in the summer](https://dylans0ng.github.io/2022/09/04/sql-progress-part-1.html). 

Anyways, without furtherado, let's dive into the main topic of this post: creating and modifying tables in SQL! 

---

## First... the basics: Data Types
If you want to make tables in SQL, you must understand the different data types that you can have. __Data types basically describe what kind of data the variable is__. For example, if you have a variable that stores a value of 5, then the __data type__ is "integer" because 5 is a number. If you have previous programming knowledge in a different language, this will make a lot of sense. 

Here's a list of some data types:

- **Boolean**: True or false
- **Character**: Char, varchar, and text
- **Numeric**: Integer and floating-point number
- **Temporal**: Date, time, timestamp, and interval
- **Array**: Stores an array of strings, numbers, etc
- **SERIAL**: Used for primary keys (which will be discussed later)

Tip: when you create a table, think about **what data type you want to use** to store the data. For example, if you want to store a column of phone numbers in a table, you should use a **text-based data type** because you can't really do arithmetic operations on a phone number. **Remember that not all numbers should have numeric data types**.

---

## Primary and Foreign Keys 

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
- Example:

Let's say we have a table called "customers":

| customer_id | payment_id | name | age |
| --- | --- | --- | --- |
| 1 | 32 | David | 24 |
| 2 | 2 | Mary | 36 |
| 3 | 40 | Sarah | 19 |
| 4 | 10 | David | 50 |

And another table called "payments":

| payment_id | payment_spent |
| --- | --- |
| 32 | 5.99 |
| 2 | 0.99 |
| 40 | 3.99 |
| 10 | 4.99 |

- In this example, the "customers" table has a **foreign key** called "payment_id". This is because it references to "payment_id", which is the **primary key** of the "payments" table. 
- Note that you can have as many **foreign keys** as you want in a table, depending on the relationships it has with other tables. 

---

## Constraints
What are **constraints**?
- Rules enforced on data columns in a table
- Constrains data in a column to adhere to certain conditions
- Used to prevent invalid data from entering a database

Common constraints:
- NOT NULL: A column cannot have a null value
- UNIQUE: Ensures that all values in a column are different
- CHECK: Ensure that all values in a column satisfy a certain condition
- PRIMARY KEY: Constraint used for a primary key

Up to this point, there has been a ton of definitions and no actual code. Don't worry; that's going to change starting from now. I am going to be creating a table with code snippets that you can use in your own SQL query editor. 

---

## CREATE Table
Alright, now let's get into the meat of this post: creating tables! 

Creating a table in SQL is actually straightforward - it may look confusing at first, but with a little practice, it will start making a lot of sense.

Here's the syntax of the **CREATE TABLE**:
```tsql
CREATE TABLE table_name (
  column_name TYPE column_constraint,
  column_name TYPE column_constraint
);
```

If we want to create a table called "customers", with a column that holds unique values for each customer and the customer's first and last name (which cannot be null), then we must do the following:
```tsql
CREATE TABLE customers (
  customer_id SERIAL PRIMARY KEY,
  customer_first_name VARCHAR(50) NOT NULL,
  customer_last_name VARCHAR(50) NOT NULL
);
```
Let's explain what the code above does:
- The **SERIAL** represents the _data type_ of "customer_id". The **PRIMARY KEY** is the constraint of the column. 
   - Primary keys should ALWAYS have the code **SERIAL PRIMARY KEY** when creating a table
- The next 2 columns, customer_first_name and customer_last_name, hold text values, so we should use the **VARCHAR** data type. 
   - The number inside **VARCHAR** represents the maximum number of characters each text value can hold. In this case, each first and last name should be no more than 50 characters.
   - **NOT NULL** is the constraint on the "customer_first_name" and the "customer_last_name" column. This is optional, but since we don't want any names to be null, we should have the constraint. This will make sure that all the values in "customer_first_name" and "customer_last_name" will exist.

Now, when you do 
```tsql
SELECT * FROM customers;
```
you will just get a blank table.

This is perfectly normal. We need to actually insert data into the table that we created, and we will do this in the next section!

---

## INSERT
The **INSERT** command allows us to **add rows to a table**. So, we can add rows to the "customers" table that we just created in the last section.

Here's the syntax:
```tsql
INSERT INTO table_name(col1, col2)
VALUES
(val1, val2),
(val1, val2);
```
After the **VALUES** statement, each set of parentheses represents **one row**. You can have as many sets of parentheses, but the more you have, the more rows that you will add.

Let's say that in our "customers" table, we want to add 3 rows. Here's how we would do it:
```tsql
INSERT INTO customers(first_name, last_name)
VALUES
('Joe', 'Smith'),
('Billy', 'Jean'),
('Bob', 'Adams');
```

The inserted values above **must match up with the constraints that we specified** in the last section.

Also note that if you're using pgadmin, you do not have to insert values into the **primary key** because the serial values will automatically be created as you insert rows into the table.

So, now that we have inserted data, we can see what our table looks like.
```tsql
SELECT * FROM customers;
```

This will return a table that looks like this:
| customer_id | customer_first_name | customer_last_name |
| --- | --- | --- |
| 1 | Joe | Smith |
| 2 | Billy | Jean |
| 3 | Bob | Adams |

Even though we've inserted data into our table, there's still more to be done! In the next section, I'll go over how to update existing data in case you want to change a value that you already added to the table.

---

## UPDATE
The **UPDATE** command allows you to change existing values of columns in a table. 

Here's the syntax:
```tsql
UPDATE table_name
SET col1 = val1,
    col2 = val2,
    ...
WHERE condition (optional);
```

The **SET** commands lets you set a column to a specific value. You can assign as many values to as many columns.

Let's use the "customers" table that we used before. In the previous section, we finally added data into our table: 
| customer_id | customer_first_name | customer_last_name |
| --- | --- | --- |
| 1 | Joe | Smith |
| 2 | Billy | Jean |
| 3 | Bob | Adams |

However, let's say that we got the first name "Joe" wrong. It turns out that the first name is actually "Jimmy". In this case, we can do the following:
```tsql
UPDATE customers
SET customer_first_name = 'Jimmy'
WHERE customer_first_name = 'Joe';
```

Basically, what the code says is that we update the table and set the "customer_first_name" column to "Jimmy" where the first name is equal to "Joe".
  - NOTE: If we didn't include the WHERE statement, all of the values inside the "customer_first_name" column would be changed to "Jimmy", but that's not what we want. **Depending on your scenario, you can include a WHERE statement or leave it out.**

Now that I've covered how to create tables and insert and update data, I will go over how to delete data from a table.

---

## DELETE
The **DELETE** command does just what is sounds: it deletes data. 

You can either delete **specific rows** or delete the **whole table**. I will go over both ways.

Here's the syntax for deleting a **specific row**:
```tsql
DELETE FROM table_name
WHERE condition;
```

The **WHERE condition** will specify which row you want to delete. For example, if you want to delete a whole row where the row_id is 1, you would say **WHERE row_id = 1**.

Here's the syntax for deleting the **whole table**:
```tsql
DELETE FROM table_name;
```

The syntax for deleting a whole a table is a lot simpler because you do not have to specify which rows to delete. 

Let's use the "customers" table to show you the DELETE command in action:
| customer_id | customer_first_name | customer_last_name |
| --- | --- | --- |
| 1 | Joe | Smith |
| 2 | Billy | Jean |
| 3 | Bob | Adams |

Let's say that we want to get rid of the whole row that holds the "customer_id" that is equal to 1 because "Joe Smith" is not a customer anymore. Here's what we can do:
```tsql
DELETE FROM customers
WHERE customer_id = 1;
```

Now, the table will look like this:
| customer_id | customer_first_name | customer_last_name |
| --- | --- | --- |
| 2 | Billy | Jean |
| 3 | Bob | Adams |

If we want to delete the whole table, then we can do this:
```tsql
DELETE FROM customers;
```

Now, the table will be completely empty: 
| customer_id | customer_first_name | customer_last_name |
| --- | --- | --- |

---

## Conclusion
If you made it all the way here, I want to thank you for your time reading this long blog post. In this post, I went over the basics on creating, inserting, updating, and deleting data in SQL. I hope you found this information useful to you and if you have any questions, please drop it down in the commentes below!.

Thank you!
