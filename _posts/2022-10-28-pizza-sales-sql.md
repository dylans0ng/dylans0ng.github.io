# Analyzing Pizza Sales using SQL (NOT FINISHED)
## Introduction
<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/112503726/198816106-57aefb24-f6f7-4c79-8ec3-1996265c77eb.png">
</p>


I did some analysis on pizza, one of the most popular foods that is a staple in America. Going to my favorite website full of datasets, Kaggle, I found a dataset on pizza sales in a fictional business (link is [here](https://www.kaggle.com/datasets/shilongzhuang/pizza-sales)).

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

I don't need any of the id columns because I am not going to make any joins since I'm only working with one table. The "pizza_ingredients" column is also useless because it doesn't help me answer any of the questions, and the ingredients vary so much in each row that it's pretty useless.

# Question 1: What days and times do we tend to be the busiest?
