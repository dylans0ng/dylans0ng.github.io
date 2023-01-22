# Excel Data Validation
![image](https://user-images.githubusercontent.com/112503726/213894830-7e6df762-c1cf-4a20-ba40-712f2e119a4b.png)

## Introduction
Whenever we deal with data, we need to make sure that the values in each column have **consistent formatting** because it will **make our lives much easier** when we start applying functions to the data. 

For example, let's say that you have **a bunch of numerical values and a bunch of numbers in text format** in the same column. If you try to get the sum of that column or whatever statistical function you use, **your results are going to be inaccurate** because the numbers in the text format will not be accounted for.

The point is: if you work with bad data, then you're going to get bad results (**garbage in, garbage out**). 

In this post, I'm going to show you how to use data validation to keep your data **clean** and **consistent**.  

## What is Data Validation in Excel?
In simple terms, data validation is basically where you **add rules to your data**.

To do this, go to the "Data" ribbon and click on "Data Validation":
![image](https://user-images.githubusercontent.com/112503726/213890247-e098b96f-8ac4-4ec7-bf10-30d77939ce69.png)

This will open up a **new window** that should look like this: 

![image](https://user-images.githubusercontent.com/112503726/213890274-cb9d1ed6-5ce5-41e8-ad9e-6489ad82cf5c.png)

## List Data Validation
If you want to add rules to a column that has text values, then you should probably use the **List Data Validation** feature. 

First, **highlight all the cells in the column** and go to the Data Validation window and click on the **dropdown arrow that says "Allow"**. From there, select "**List**" from the options:

![image](https://user-images.githubusercontent.com/112503726/213890632-96a52c01-e13a-458a-9a70-b2723fcc29b8.png)

Then, decide **what text values you want your column to be limited to**. For example, look at this table:
![image](https://user-images.githubusercontent.com/112503726/213890981-dd223fd5-e73a-464c-b237-9dd7bf294227.png)

Caption: Credit to Udemy's Excel Beginner to Advanced 

Let's say that I want to **include only the text values** "Chevy", "Oldsmobile", "Chrysler", "Pontiac", "Ford", and Dodge" in the "**Make**" column. I would type these values into the "Source" box and **separate each of them by a comma WITHOUT ANY SPACES**:
![image](https://user-images.githubusercontent.com/112503726/213892383-9958e009-361b-490b-9e80-21e5a133a22c.png)

This will ensure that all of your data in the column will **ONLY INCLUDE the list of values that you specified** in the "Source" box:
![image](https://user-images.githubusercontent.com/112503726/213893216-469b55f6-8fe8-4e83-a38d-1a4708e96e06.png)

## Decimal Data Validation
Data validation with decimals **works exactly the same way** with list data validation, but this time, you are **adding rules to numeric values**.

As an example, here's a look at the table again:
![image](https://user-images.githubusercontent.com/112503726/213894526-8c2718a6-2a4d-49b1-b8a2-5199c54265b1.png)

Caption: Credit to Udemy's Excel Beginner to Advanced

Let's say I want the "Rate" column to only be able to have **numeric values between 1.50 and 50.50**. To do this, **highlight the cells that you want to add the rule on** and open the Data Validation window. Make sure to click on **"Decimal" in the "Allow" dropdown box** (but you can do whole number if your data doesn't have any decimals):

![image](https://user-images.githubusercontent.com/112503726/213894605-0609129c-2b46-4012-ab86-95c3149d7f0b.png)

If you enter any value that **falls outside of the numeric range that you set up**, then you will get an error:
![image](https://user-images.githubusercontent.com/112503726/213894732-1bb9cee3-d231-4acd-ad42-f95cd39682f6.png)

Excel also **won't let you enter in any text format** values:
![image](https://user-images.githubusercontent.com/112503726/213894752-a6b4ed6a-46e7-4af6-888b-d268df57ef5c.png)

## Conclusion
That's it for this post! I hope you learned something new that you can do in Excel. I've only scratched the surface, and I encourage you to play around with the different rules that you can do with the Data Validation feature. Anyways, thank you for reading this post and I hope you have a good day!
