# Analyzing Pizza Sales using SQL 
## Introduction
<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/112503726/198816106-57aefb24-f6f7-4c79-8ec3-1996265c77eb.png">
</p>


I did some analysis on pizza, one of the most popular foods that is a staple in America. Going to my favorite website full of datasets, Kaggle, I found a dataset on pizza sales in a fictional business (link is [here](https://www.kaggle.com/datasets/shilongzhuang/pizza-sales)). I first used SQL to **analyze data** and **gain insights** from the dataset and then used Power BI to create **visuals that summarize my insights** that I obtained. 

To make my job even easier, the Kaggle dataset provided me with sample statistical questions to answer, so I played around with the data to answer them:
## Statistical Questions
1. What days and times do we tend to be busiest?
2. How many pizzas are we making during peak periods?
3. What are our best and worst-selling pizzas?
4. What's our average order value?

## The Data
The dataset was in a form of a csv file (comma separated value). Here is an image of the original data (first 10 rows):
![image](https://user-images.githubusercontent.com/112503726/198855490-044d6f5b-8e6d-4c71-83a0-3ac36af3070f.png)

There are 12 total columns:
- order_details_id
- order_id
- pizza_id
- quantity
- order_date
- unit_price
- total_price
- pizza_size
- pizza_category
- pizza_ingredients
- pizza_name

I imported the data into pgadmin so that I can make SQL queries and gain insights from this pizza data.

Here's what it looks like in pgadmin:
![image](https://user-images.githubusercontent.com/112503726/198855763-d4444694-3cff-4e42-8745-580671d4e2c1.png)


## Data Cleaning
As always, I cleaned the data before I dove deep into it. 

Columns that I don't need include:
- order_details_id
- order_id
- pizza_id
- pizza_ingredients

```tsql
ALTER TABLE pizza_sales
DROP COLUMN order_details_id, 
DROP COLUMN order_id, 
DROP COLUMN pizza_id, 
DROP COLUMN pizza_ingredients;
```
I don't need any of the id columns because I am not going to make any joins since I'm only working with one table. The "pizza_ingredients" column is also useless because it doesn't help me answer any of the questions, and the ingredients vary so much in each row that it's pretty useless.

# Question 1: What days and times do we tend to be the busiest?
First, I want to see the different years that this dataset covers:
```tsql
SELECT DISTINCT(EXTRACT(YEAR FROM order_date)) FROM pizza_sales 
```
Result:

![image](https://user-images.githubusercontent.com/112503726/198856341-115d67f5-6f30-47f7-bb02-6f11593f98cc.png)

This means that this dataset covers the pizza sales in the business in 2015 only. 

Now, I wanna see **what time of the day** is the business selling the most pizza:
```tsql
SELECT EXTRACT(HOUR FROM order_time) AS time_of_day, SUM(quantity) AS quantity_sold
FROM pizza_sales
GROUP BY EXTRACT(HOUR FROM order_time)
ORDER BY SUM(quantity) DESC;
```
Result:

![image](https://user-images.githubusercontent.com/112503726/198856546-391f5c06-a2be-43e0-87f9-bca10c43d67b.png)

The top 3 times where the most pizza is sold seems to be "12", "13", and "18". In context, I think it means that 12 means 12 pm, 13 represents 1 pm, and 18 represents 6 pm. It seems like the pizza business is the busiest during around lunch and dinner time since it gets the most pizza orders from customers during these times.

To find **what day of week** is the busiest, I used a function called **TO_CHAR** to convert all the dates in the column to a day of week.
```tsql
SELECT TO_CHAR(order_date, 'Day') AS day_of_week, SUM(quantity) AS quantity_sold
FROM pizza_sales
GROUP BY TO_CHAR(order_date, 'Day')
ORDER BY SUM(quantity) DESC;
```
Result:

![image](https://user-images.githubusercontent.com/112503726/198856810-0ec293ef-8bfd-47c8-846f-ebcf47348c50.png)

Friday is the busiest day of the week since the business is selling the most pizzas on Fridays. 

## Question 2: How many pizzas are we making during peak periods?
I wanna get the top 3 peak periods in this pizza business (note this code is the same as the one above):
```tsql
SELECT EXTRACT(HOUR FROM order_time), SUM(quantity) 
FROM pizza_sales
GROUP BY EXTRACT(HOUR FROM order_time)
ORDER BY SUM(quantity) DESC;
```
Result:

![image](https://user-images.githubusercontent.com/112503726/198932290-f5ee3d12-a9bf-42eb-ac56-9630f3f0d56d.png)

This tells me that the top 3 peak periods are the **12th, 13th, and 18th hour**.

Now, I'm going to find the sum of all the pizzas sold in those 3 periods:
```tsql
SELECT SUM(quantity) AS pizza_sold_in_top_3_peak_periods
FROM pizza_sales
WHERE EXTRACT(HOUR FROM order_time) IN (12, 13, 18);
```
Result:

![image](https://user-images.githubusercontent.com/112503726/198932620-75437434-bb73-4e01-bab0-122677630107.png)

I just used a simple **SIMPLE WHERE** statement to answer the statistical question. Based on the result, 18,606 pizzas were sold in the top 3 peak periods.

## Question 3: What are our best and worst-selling pizzas?
I'm going to find the **top 3 best selling pizzas** and **the bottom 3 worst selling pizzas**. It's a pretty simple query: just use a **GROUP BY** clause. 

Top 3 best selling pizzas:
```tsql
SELECT pizza_name, SUM(quantity) 
FROM pizza_sales
GROUP BY pizza_name
ORDER BY SUM(quantity) DESC
LIMIT 3;
```
Result:

![image](https://user-images.githubusercontent.com/112503726/198933990-e3ca892c-bbc4-472f-b86a-8342e238cacd.png)

Bottom 3 worst selling pizzas:
```tsql
SELECT pizza_name, SUM(quantity) 
FROM pizza_sales
GROUP BY pizza_name
ORDER BY SUM(quantity) ASC
LIMIT 3;
```
Result:

![image](https://user-images.githubusercontent.com/112503726/198934124-c53a3612-1588-44c0-b9a0-b3d0270295b4.png)

Based on these two queries, the top 3 pizzas are "Classic Deluxe", "Barbecue Chicken", "Hawaiian". The bottom 3 pizzas are "Brie Carre", "Mediterranean", "Calabrese". I used the **ASC** and **DESC** feature in the **ORDER BY** statement to get the top and bottom 3 pizzas. 

## Question 4: What's our average order value?
This doesn't answer the question, but I'm just interested in the average prices for the pizzas based on the size:
```tsql
SELECT pizza_size, AVG(total_price) AS average_total_price
FROM pizza_sales
GROUP BY pizza_size
ORDER BY AVG(total_price) ASC;
```
Result:

![image](https://user-images.githubusercontent.com/112503726/198935267-4870f516-d25c-4ade-bc55-d7b09ecf6fde.png)

Clearly, the average prices of the pizzas increase as the size increases, which makes sense.

Now, I'm going to answer the question to find the **average price of ALL pizzas, regardless of size**:
```tsql
SELECT AVG(total_price) AS average_total_price
FROM pizza_sales;
```
Result:
![image](https://user-images.githubusercontent.com/112503726/198935697-463bfa20-434e-4137-b48f-a8bbd7e22354.png)

The average price of all the pizzas is about $16.82, which is a pretty reasonable price for a pizza in my opinion. 

## Conclusion
If you have reached this part, I want to thank you for reading my whole post. This was a pretty simple project, but despite its simplicity, I feel more proficient in the SQL language and more confident as I write these queries. I'm thinking of posting something related to Power BI next, but if you have any other ideas of what I could post, feel free to comment it down below!

Thank you!
