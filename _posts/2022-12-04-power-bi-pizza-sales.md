# Pizza Sales Project with Power BI (UNFINISHED)

![image](https://user-images.githubusercontent.com/112503726/204071711-67ca7787-bdb3-4bd0-805c-a99dbf820071.png)

## Introduction
Welcome to my first project using Power BI! 

A month ago, I analyzed the Pizza Sales [dataset](https://www.kaggle.com/datasets/shilongzhuang/pizza-sales) from Kaggle by creating SQL quieries; you can check out that post [here](https://medium.com/@dylanhgs/analyzing-pizza-sales-using-sql-1550fb7a93de). However, this time, I will **analyze the same dataset by creating visuals** instead of queries. 

## Connecting the Data 
Because I previously used a SQL database to analyze the pizza sales, I'm going to **connect that database into a Power BI report**. 

So, I will click on "Get Data" on the home ribbon and click on the "PostgresSQL database" button, like so:
![image](https://user-images.githubusercontent.com/112503726/204120902-b1d05997-357b-4684-8f36-42adc48ae668.png)

Then, I put the SQL server and database name:
![image](https://user-images.githubusercontent.com/112503726/204120934-c8eb400a-34c1-4859-8f03-6915f3f44003.png)

After that, I got this pop-up window:
![image](https://user-images.githubusercontent.com/112503726/204121034-9f842dcd-528f-4317-8118-7eb35e09c763.png)

Usually I would click on "Transform data" but because **I already cleaned the data in the SQL database,** I will just click on "Load".

## Data Model
I don't have to make any changes in the **data model**. Looking at the image, this is a pretty simple project and **there is only one table involved**, so there isn't any relationships that need to be established:
![image](https://user-images.githubusercontent.com/112503726/204121170-08ca2a57-b3b9-4470-ae0c-69d719d445b7.png)

So, I can now **dive into creating visuals** for this dataset. However, before I do that, I'm going to revisit the statistical questions that I used in the SQL post:
## Statistical Questions
1. What days and times do we tend to be busiest?
2. What are our best and worst-selling pizzas?
3. What's our average order value?

I'm going to be showing you a **visual that answers each statistical question**, and after that, I will show you what my report looks like **as a whole**.

## Statistical Question 1: What days and times do we tend to be busiest?
I need to use **DAX** in order to answer this question. There's a DAX function called **HOUR** that retrieves all the hours from **timestamps**. So, here's what I did.

I have a column called "order_time" that has **all the timestamps** of when each pizza was ordered. This is what the code looks like:
![image](https://user-images.githubusercontent.com/112503726/204455298-764d92a3-6eeb-4492-ae0d-b872ac719336.png)

Then, I created a **simple bar chart** that shows the **relationship** between the hour and the quantity of pizzas sold:
![image](https://user-images.githubusercontent.com/112503726/204456915-40459465-5b4d-41c6-a485-240e487bd1ae.png)

Looking at the chart, the busiest time for this fictional pizza business is the **12th hour**, which is noon.

I also need to show what the busiest day for the business is. To do this, we need to use more DAX!

I created a **new column** using the DAX function callled **WEEKDAY**:
![image](https://user-images.githubusercontent.com/112503726/205429230-35899fb9-55e3-45b5-8ae2-ba6baaa72579.png)

This basically returns integers from the dates in the column called "order_date". The **integers range from 1 to 7** with 1 representing "Sunday" and 7 representing "Saturday". However, I want to **convert these integers to the actual days of the week**, so I will have to use another DAX function called **IF**:
![image](https://user-images.githubusercontent.com/112503726/205469391-cf54a47d-2ba0-4a04-80a3-4269e925ca9b.png)

Here, I created a new column that contains the **actual names of the days of the week** based on the numbers from 1 to 7. 
![image](https://user-images.githubusercontent.com/112503726/205469529-76f110e3-7d0f-481e-ba36-9b319482bef5.png)

This bar chart shows that **Fridays, Saturdays, and Sundays** sell the most pizzas. 

## Statistical Question 2: What are our best and worst-selling pizzas?
**BEST SELLING PIZZAS**
To answer this question on Power BI, I used the "pizza_name" and "quantity" column. Because there are many values in the "pizza_name", I **used a filter to only show the 5 pizzas that are sold the most**. This would reduce clutter in the bar chart. 
![image](https://user-images.githubusercontent.com/112503726/205469782-1a9f5831-c604-4348-afa4-c791b062d345.png)

Here's what the visual looks like:
![image](https://user-images.githubusercontent.com/112503726/205469851-32184e6f-179e-4940-a66b-aa2f0c2aec56.png)

There doesn't seem to be much difference in the number of pizzas sold for the top 5 types. Nevertheless, based on the chart, "Classic Deluxe Pizza" seems to be the popular choice among the customers. 

**WORST SELLING PIZZAS**
I used a filter again, but this time, I filtered the **bottom 5 pizzas sold**. 
![image](https://user-images.githubusercontent.com/112503726/205469997-60133bad-8f67-4d7e-8b32-5d3105d6be3e.png)

Here's how it looks:
![image](https://user-images.githubusercontent.com/112503726/205470001-ff8ac2ca-01db-4eca-87fa-4eb3b39abb02.png)

The "Brie Carre Pizza" seems to be the least popular pizza in the business with only 490 of them being sold.

## Statistical Question 3: What's our average order value?
I'm going to find the average price for the pizzas **based on the size**. So, I'm going to use the "pizza_size" and "total_price" column to answer this question. 

I made a treemap:
![image](https://user-images.githubusercontent.com/112503726/205470740-1878a87f-bd35-4f6b-9316-77ce09792388.png)

Not surprisingly, **the bigger the size of the pizza, the more expensive the average price is**. The XXL pizza size has the most expensive average price of $35.95.

## The Final Report
I played around in the Power BI Report and polished the visuals that I showed above and did my best to make it visually appealing:
![image](https://user-images.githubusercontent.com/112503726/205553915-cc0dba6b-30f6-4f61-a92f-f71426247f6d.png)


## Conclusion
Thank you for reading this post! I hope you enjoyed it. If you want to see my other content related to Power BI, check out this previous [post](https://medium.com/@dylanhgs/what-is-power-bi-4af26ec0a9cd). 
