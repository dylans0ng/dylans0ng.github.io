# Create a TIMELINE SLICER for your Excel Dashboard!
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/f147ec90-e12d-4b76-aada-3b0dabca0e62)

## Intro
In this blog post, I'll show you how to create a **timeline slicer** in Excel. It's a pretty useful tool that will **make your dashboard more interactive**, especially if you have a timeline graph, because as you click on the different buttons on a timeline slicer, the **values on all your other visuals will change** based on the buttons you press. 

I'll explain more on this later, so keep reading!

## What is a timeline slicer?
A timeline slicer is a **filtering tool** lets you see values based on the **certain dates or times** that you filter on. You'll see how it works in this example I'm about to show you...

## Introducing the Dataset
To use the timeline slicer, I'm going to use a Kaggle dataset on **Netflix movies and TV shows** that you can find [here](https://www.kaggle.com/datasets/maso0dahmed/netflix-movies-and-shows).

Here's a quick glance at the data:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/7210e621-c397-44a0-9f5e-dc9055525271)

I formatted the **"release_year"** column as a date, which is going to be important for later. Also, I noticed that for some reason, **all the dates are inaccurate** because none of these movies and TV shows came out in 1905. They came out wayyy later. 

However, I'm still gonna work with it because the point of this blog post is to show you **HOW to create a timeline slicer**, and you can apply this process to **ANY other dataset**.

## Creating the Pivot Table
Before we create the timeline slicer, we have to first build a **simple pivot table**. So, click on the "Insert" ribbon and click on the **"Pivot Table"** button on the top left-hand corner:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/e9553264-52fe-49e2-bdcd-446c4f98c9be)

Make sure that the **whole data** is selected inside the range and click on "OK":
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/8dd9ed7e-4344-45cd-bfe5-5147c5aa6643)

Doing that's gonna create a new worksheet where you can **build the pivot table**.

## Building the Pivot Table
Inside the new worksheet, I'm going to drag the "age_certification" column into the **"Rows"** box and the "runtime" column into the **"Values"** box:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/d2c61446-982b-4113-8715-788f6b700ac7)

But I don't want to get the SUM of the runtime values. I want to get the **AVERAGE**, so I'm going to click on the dropdown arrow next to "Runtime" and click on **"Value Field Settings"**. From there, I'll click on **"Average"**:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/4ffa1745-daf2-4db6-a822-cadde027532d)

Here's what my pivot table looks like:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/15b5ec95-160b-4e63-8495-b2fff08d6e44)

After you've finished building your pivot table, you can move on to the main part, which is **creating the timeline slicer**.

## Creating the Timeline Slicer 
Make sure you're **selected inside the pivot table** and go to the "PivotTable Analyze" ribbon and click on the button that says **"Insert Timeline"**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/b66c7b65-9e77-4a5f-bc72-17d64d9a4370)

This is going to open a new pop-up window, and it shows the **"release_year" column**, so I'll check that box:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/bed6f9fb-6e1b-402e-ac8f-b28f4fab3306)

If I didn't format the "release_year" column as a date before, then **this wouldn't have worked** because I can only create a timeline slicer **if one of the columns are formatted as a date** in the dataset.

Anyways, here's what the timeline slicer should look like:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/6f2d4b3f-f1c8-428f-88e4-aec5c59bd13c)

But there's only one year in this whole dataset, so I'm going to change the timeline slicer to **display the quarters** instead of the years. So, I'll click on the dropdown arrow next to "YEARS" and **change it to "QUARTERS"**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/4f20c92d-0cef-4f37-b73e-40fedc9a1539)

That's going to show you **4 quarters of the year**, and you can click on each different quarter, which will **change the values on the pivot table** based on the quarter you select.  

## Video on Creating a Timeline Slicer
If you want to see a **more interactive version** of this blog post, check out a [video](https://youtu.be/eiIn1eVvUjc) that I made. It's a 5-minute video that will **walk you through all the steps** of creating a timeline slicer.

I hope to see you over there, and thank you so much for reading! 
