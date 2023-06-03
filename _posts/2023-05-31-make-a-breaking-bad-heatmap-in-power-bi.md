# Make a Breaking Bad Heatmap in Power BI
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/734fa027-7938-4278-aaf0-bb586446813a)

make a table of contents that shows each section with the end result 

## Introduction
Breaking Bad is one of the **top rated TV shows**, so I decided to make **a heatmap** that shows the IMDB ratings for each episode in the 5 seasons. 

In this post, I'll quickly show you how to **easily make this heatmap**, and you'll learn how to **create a matrix** and **apply color formatting** to the values inside the matrix. 

I'll be using Power BI to make this visual, but at the end of this post, I'll show you how you can build the same thing in Excel. 

## Where I got the Data
I did not make this dataset myself. Thank you so much to whoever compiled all the information on each Breaking Bad Episode: https://www.kaggle.com/datasets/varpit94/breaking-bad-tv-show-all-seasons-episodes-data

## Preparing the Data
Before I start making the visual, I need to clean up the data by getting rid of any unncessary columns. Now, when import the data from your local computer onto Power BI, make sure to hit "**Transform Data**".

This will open up the **Power Query Editor**, which should look like this:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/de471d3d-6911-4cb1-8cb8-77cbe9dc6f22)

Here, we can **make changes** to our dataset. I'm going to get rid of ALL of the columns **except for the ones** called "Season", "Episode", and "Rating_IMDB".

To get rid of columns, right click the column name and hit **"Remove"**. You should see the step show up on the "Applied Steps" pane: 
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/5e6a1418-ca0f-40b9-88c5-673c4a69111c)

So, after you remove all the columns, you should be left with **3 columns**.

Now, hit **"Close and Apply"** on the top left corner:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/6ca8e84c-f0f7-4cc8-8736-42e810ee7031)

We're ready to move on to the next step...

## Making the Heatmap
Before we do anything, make sure that you're in the "**Report**" tab that looks like this:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/9705a6b8-1417-42fa-bf88-c0e85f24f4d2)

### Creating the Basic Matrix 
First, we need to make **a matrix** that will display all the IMDB ratings:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/e936df43-703d-48d0-8e1a-177ebaede84a)

This will open a **blank matrix**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/ab3dfe42-da29-4a70-b2e6-24b5edf49650)

Now, drag "Episode" from the data into the **rows of the matrix**, drag "Season" into the **columns of the matrix**, and drag "Rating_IMDB" into **the values of the matrix**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/15fb52a2-f710-4b3e-badc-5a91e37b36c5)

This is what the result looks like so far:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/4f2e2909-d273-4081-b742-b1fd09ef1561)

### Styling the Matrix 
This is optional, but the numbers in the matrix look pretty ugly right now. You can make them **look cleaner** by changing the style to "Minimal": 
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/acd78bb0-36c1-4f4d-abb4-394260400b31)

In my opinion, the matrix looks a lot better now! 
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/b7301672-6181-4153-a3cb-5542c7e9b1bf)

The "Total" columns look pretty annoying, let's remove that by toggling "**Column subtotals**" and "**Row subtotals**" off:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/0612825f-6c42-4193-8c67-5791433d8d0e)

Now, the matrix looks a lot better!
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/ffd26914-6afe-46cb-96d6-5a48cfe14d54)

### Adding Color 
This isn't a heatmap **until we add color** to it. To add a **color gradient** to this matrix, go to "**Cell elements**", and then toggle the "**Background color**" on, like this:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/a897039e-c566-4f2a-a47a-441f5f247d66)

Here's what it looks like now:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/4a0b2fd6-09dd-428b-8ef9-e4704e3e06b5)

But the **Breaking Bad color theme** isn't really about blue. It's more of a **combination of yellow and green**, so that's what my color gradient is going to be.

TYPE THIS IN LATER: Click on "Fx" and sele the color of your choice!
