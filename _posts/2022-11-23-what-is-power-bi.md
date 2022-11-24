# What is Power BI? 

![image](https://user-images.githubusercontent.com/112503726/202890187-9ce0eb36-1568-4836-94f8-d7dc5146048f.png)

## Introduction
Throughout this month, I've posted many projects that involved wrangling data through SQL. However, I am going to shift gears and start playing around with a data visualization tool called **Power BI**. 

Power BI is a great way to gain insights from your data as it is much easier to understand large amounts of numbers by **looking at visuals** rather than looking at rows and columns of data. 

I've chosen to use Power BI because I love the GUI of the app, and it is very easy to learn; there are many free tutorials online that could get you started.

In this post, I'm going to walk through the **main features of the Power BI Desktop app**, so if you're interested in learning about the basics of this powerful data visualization tool, keep reading! 

## Workflow within Power BI Desktop
Power BI Desktop is the app that is free for anyone. You can many things with the free version such as **cleaning data, creating visuals, and managing relationships between tables**. However, the downside is that you cannot collaborate together with others and share your work to the public. To do that you must use a paid version called Power BI Pro.

I'm only going to be focusing on Power BI Desktop since anyone has access to it.

There are **3 main steps** when working inside Power BI Desktop:
<p align="center">
  <img width="1000" height="300" src="https://user-images.githubusercontent.com/112503726/202918843-c95857cb-7ce7-4f49-9d18-1b2c009c2f38.png">
</p>

1. **Query Editor** (Connect the data, cleaning data phase)
2. **Data Model** (manage relationships)
3. **Report** (make visuals)

I will explain the function of each step and how it looks like in the app.

## Query Editor
This is the first step in the workflow. You can't create any visuals if you do not have any connected data! Therefore, **you must know how to import your data**.

Once you open the Power BI Desktop, go to the "Home" button and **click on "Get Data"**. It looks like this:
![image](https://user-images.githubusercontent.com/112503726/202919490-34e884fc-b2d6-4871-b4e3-9baa5d053e6d.png)

There, you can import your data from various sources such as **Excel, SQL Server, Microsoft Access, and many more**. It's cool how Power BI can connect to data from so many different servers. 

After you click on the dataset that you want, you will see a pop-up appear on your screen. On the bottom of the pop-up, you will see three options "**Load**", "**Transform Data**", and "**Cancel**". 

![image](https://user-images.githubusercontent.com/112503726/202919790-cb1abe50-53b6-41ba-a581-a447553d48d4.png)

Even though the "Load" button may look more appearing, **don't click it**! You should click on "Transform Data" first because **you want to be able to clean your data** before you load it onto Power BI.

Once you click on "Transform Data", a new window will appear. This window is called the "**Query Editor**". It looks something like this:
![image](https://user-images.githubusercontent.com/112503726/202920887-809d2e67-0478-4a68-a65a-c282b0d982cf.png)

Here, you can clean data by **removing null values, changing the format of the columns, etc**. 

After you're done with cleaning, you can click the "**Close & Apply**" button on the top left corner of the Query Editor and you're ready to move on to the next step!

## Data Model
After you have imported and cleaned the data in the Query Editor, you can now head over to the Data Model. It looks like this:
![image](https://user-images.githubusercontent.com/112503726/203484405-2600b232-f0ac-48d1-9879-05c8d2f5b344.png)

If you have more than one table in your database, it is important to **create relationships** between them in order to display the correct information in your visuals. 

The Data Model is cool because it shows you a **nice diagram** of all the tables and the relationships between them. Here's an example:
![image](https://user-images.githubusercontent.com/112503726/203484911-1fdb275f-7aae-4bbc-b4a3-3c9d90313049.png)

You can also use **DAX** formulas to create **new measures** and **new columns**. You can do this by clicking on the "Home" ribbon like so:
![image](https://user-images.githubusercontent.com/112503726/203700958-f5defb3f-7225-42e2-a1c0-ba0423bd5a41.png)

DAX stands for **Data Analysis Expressions** and can help you gain new information from the already existing data that can help you make your visuals in the next step. **DAX** is probably one of the most important things that you should learn because there are a wide variety of powerful functions such as SUMX(), AVERAGE(), COUNTROWS(), and many more. 

## Report
This is my favorite part of the process. If you love art, now is your time to shine. You can create **stunning visuals that answer any statistical questions** that you have. 

To go to the "Report" tab, go to the left hand side and click on the little icon at the very top:

![image](https://user-images.githubusercontent.com/112503726/203702302-153caf6e-6ea2-44f4-91aa-ddb6f5a04e93.png)

What I love about this stage in the workflow is that **you can be as creative as you want** in your visuals. 

Here's an example of a report that I made in my free time:
![image](https://user-images.githubusercontent.com/112503726/203702688-e4aca63b-1eaa-434f-9c56-219a90486e93.png)

The colors and charts/graphs make it **very easy for others to gain insights** from the data just from a quick glance at the report.

## Conclusion
I hope you liked my overview of Power BI! In my next post, I will create a full visual report on the **Pizza Sales SQL project** that I did in a previous post over [**here**](https://dylans0ng.github.io/2022/10/28/pizza-sales-sql.html), so stay tuned for that!

Anyways, I hope you have a good day and thank you for reading! 

