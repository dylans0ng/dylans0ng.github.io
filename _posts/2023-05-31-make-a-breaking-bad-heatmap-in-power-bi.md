# Make a Breaking Bad Heatmap in Power BI
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/734fa027-7938-4278-aaf0-bb586446813a)

make a table of contents that shows each section with the end result 

## Introduction
In this post, I'll quickly show you how to easily make a heatmap that shows the IMDB ratings on each episode in the famous TV Show "Breaking Bad". I'll be using Power BI to make this visual, but at the end of this post, I'll show you how you can build the same thing in Excel. 

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


