# 3 Simple Visuals in Python
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/8e1ab7ee-7da3-4901-9a86-fc5d11d12f82)
(From Lukas Blazek on Unsplash)

## Introduction
It's much easier to gain insights by **looking at visuals**, rather than looking at rows and columns of data. So, in this post, I'll share 3 visuals that you can make **using the Seaborn library**, which is provided by Python. 

## The Dataset 
As a demonstration, I'll be using a dataset on all the **pro tennis matches in 2022**. Here's the link, if you want to follow along: https://github.com/JeffSackmann/tennis_atp/blob/master/atp_matches_2022.csv 

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/999e90a0-295b-46d5-9c25-b0451534a876)
(From Moises Alex on Unsplash)

## Importing the Libraries and Dataset in Python
In the first cell of our Jupyter notebook, we're going to import **3 libraries**: Pandas, Seaborn, and Matplotlib.
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/f05c105d-5544-4e33-84d6-fcbc95210ca5)

Pandas will allow us to **load our tennis dataset**, and Matplotlib is needed since **Seaborn is built on top of it**. 

To load the dataset with Pandas, we say this:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/9b6655b1-e929-4a51-be84-c2df00e15788)

By running this line of code, we've created a Pandas dataframe called "**df**". The **.read_csv** method takes in the file name of the dataset, and it'll be different for you depending on **where you have saved it on your local machine**. 

Now, we are ready to create visuals from our dataframe, and it's quite simple! 

## Countplot 
The first visual I'll make is a **countplot**. This is basically a simple bar chart that counts the number of **unique values in a categorical variable**.

We're gonna use one of the methods from Seaborn called **.countplot**. Here's what it looks like in Python:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/fab21dc0-fc60-4469-8f80-cb3027107295)

The **second line of code** creates the countplot. The first argument inside the .countplot method is **the dataframe**, which was "df". In the second argument, you must provide **what column you want to see be counted**, which was "surface".

The third line of code basically **sets a title to the graph** called "Number of Tournaments by Surface", using the **.title** method provided by Matplotlib.

The first line of code **changes the color theme** of the graph. In this case, I used the "**darkgrid**" style. It's completely **optional**, and it's up to you whether you want to include it or not.

Here's what the countplot looks like:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/084ce45a-5dc4-46ff-86c9-60eabf2e8e9c)

It's a very simple visual, but just by glancing at it for 1 second, you can already see that **hard courts were the most common surface** in tennis tournaments in 2022.

## 2 More Visuals!
If you want to know how to create the last 2 types of visuals (**a scatterplot and a boxplot**), then make sure to check out the video below. I've provided **timestamps** in the description so you can skip around the video. Feel free to let me know if there are any questions that you have! 

https://youtu.be/sPxQQya92dE
