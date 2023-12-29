# Export Data in Python with ONE LINE of Code!
## Introduction
If you want to permanently **save some part of a dataset**, then there's a pretty easy way to do that in Python. This blog is going to show you how to **export any data** from your Python editor into your local computer.

So, let's get into it!

## The Dataset
For this blog, I'll use a Kaggle dataset on **Netflix movies and TV shows**. You can click [here](https://www.kaggle.com/datasets/maso0dahmed/netflix-movies-and-shows) to download the data and follow along! 

## Importing the Pandas Library
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/b98b9140-8c42-4066-b46b-a0e6262bfa0f)

This will import the Pandas library, which will allow us to **import the dataset from Kaggle into Python**.

## Importing the Kaggle Dataset
To load the Netflix dataset, I have to use a method from pandas called **read_csv()**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/f1625cad-ec18-4fca-9619-c6e0d5208c68)
Here, I just passed in the **name of the file** into the read_csv() function and stored it into a variable called **df**.

I also said **df.head()** because I wanted to take a **quick look** at the dataset. The **head()** method basically returned the **first 5 rows**.

## Creating a New Dataframe
Now that I made a dataframe called "df", I can create another dataframe from the existing one. 
DO THIS LATER!


