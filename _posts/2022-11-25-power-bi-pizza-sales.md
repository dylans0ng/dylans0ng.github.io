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

So, I can now dive into creating visuals for this dataset. However, before I do that, I'm going to revisit the statistical questions that I used in the SQL post:
## Statistical Questions
1. What days and times do we tend to be busiest?
2. How many pizzas are we making during peak periods?
3. What are our best and worst-selling pizzas?
4. What's our average order value?

I'm going to be showing you a **visual that answers each statistical question**, and after that, I will show you what my report looks like **as a whole**.

## Statistical Question #1

## Conclusion
Thank you for reading this post! I hope you enjoyed it. If you want to see my other content related to Power BI, check out this previous [post](https://medium.com/@dylanhgs/what-is-power-bi-4af26ec0a9cd)
