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
Let's say that I want to create a separate dataset on ONLY the Netflix movies and NOT the TV shows. Using the dataframe I just created before, I can create **another dataframe** from the **existing one**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/39f700d0-1873-4de2-8dbc-ffb45f988bbe)

Here, I created a new dataframe called **"df_movies"** and say that it's equal to "df", **as long as df['Type'] is equal to 'Movie'**, which is indicated by the conditional inside the square brackets.

So, this line of code created another dataframe that stored data on **only the Netflix movies**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/8af5ed1e-7411-4b7d-ae7a-9676c11ed41e)

## Exporting the Data
Now, I'm finally going to **export** this new dataframe, and it'll only take **one line of code**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/3a5e979d-6607-4068-8633-c66078022909)

In this cell, I used the **to_csv()** function from Pandas, which would automatically save the Pandas dataframe as a **local csv file**. And the name of the csv file would be called **"netflix_movies.csv"** because that's what I passed inside the to_csv() **argument**. 

So, after I ran that, I got that dataframe saved into my **local folder**, the same one as the one my Python program was located in.

## Outro
Alright, that's it for this blog! Hopefully you learned something new and **if you learn better by watching a video**, then check out this [video](https://youtu.be/bybxYHRRYKM) that I made. 

I hope to see you over there, and thanks for reading!
