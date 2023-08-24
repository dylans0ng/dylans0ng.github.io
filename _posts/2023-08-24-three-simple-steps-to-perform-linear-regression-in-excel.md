# 3 Simple Steps to Perform Linear Regression in Excel
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/f39fd730-2752-4a3e-ae45-6e371923d4b8)

## Introduction
In this blog post, I'll show you **3 simple steps** to create a linear regression model in Excel. Linear regression is important because it can tell you **important trends** between two or more variables in the data. So, let's get started!

## The Dataset
The Kaggle dataset I'll use in this post shows all the **sale prices for the houses in the King County area** (or the Seattle area). Here's the download link, if you want to follow along: https://www.kaggle.com/datasets/harlfoxem/housesalesprediction
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/969fd428-72d4-43ad-8935-b975201be5b1)
(Credit to Thom Milkovic on Unsplash)

## Step 1: Come Up with Your Statistical Question
Before we create the model, we need to know what variables we're interested in. For this video, my question is going to be "**What is the relationship between the square feet in the living room and the price?**"

So, my variables are going to be the **square feet** and the **price**. You can choose your own variables, but you need to make sure that they're **continuous variables**, or else you're gonna run into a problem.

Now, we need to know what our **independent**, which is on the x-axis, and our **dependent**, which is on the y-axis, variables are. In this example, it makes sense to have the **house price as the dependent variable** because we're assuming that the number of square feet in the house is going to **affect** what the price is.

In the next step, we're going to hop over onto Excel.

## Step 2: Selecting the 2 Columns of Interest in Excel
First, you have to select the **second cell** in the column that has all the square feets and then do **Ctrl+Shift+Down**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/c8a43289-6465-4fb3-a38a-440efd38406f)

Then, hold the **Ctrl** key and click on the second cell in the price column and do **Ctrl+Shift+Down** again:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/d617b9ed-a467-498f-9e6b-8d3a7cfeea8c)

## Step 3: Create the Scatterplot
Now, go to "Insert" and click on this button over here:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/ed7e2f26-d452-486d-83e2-04828538462b)

But, there's actually a problem:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/bce6bf19-3e7c-4b73-8fe6-30a253903d4b)

You can see that all the prices are on the **x-axis**, which is NOT what we want.

So to fix this, you have to right-click on the graph and click "**Select Data**":
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/7b7db17f-4704-4b1a-8d88-937b1d4246d7)

This is going to open a new window that looks like this:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/d8084b61-8c83-45ff-aa6c-f2dfba8e2837)

From here, click on "**Edit**". This is going to open another window:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/3f66ab67-782e-449b-a845-9b90db26c90e)

In the "**Series X values**" box, get rid of everything inside and starting from the 2nd cell, highlight all the values in the **square feet** column. In the "**Series Y values**" box, do the same thing but this time, highlight all the values in the **price** column. 

So, the boxes should look like this:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/8fdc7778-27a5-4873-b120-0081d0db2ed3)

Now, the scatterplot looks a lot better now, with the **square feet** on the x-axis and the **prices** on the y-axis:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/5dc47dee-38fb-4c5b-9734-6643688ba46c)

## Want to See More?
If you want to see me create a **regression line** over this scatterplot and **analyze** what the model tells us, check out my full video!

(Insert the link) 

So, I hope to see you over there! 
