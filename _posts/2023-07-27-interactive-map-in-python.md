# How to Create Interactive Maps in Python
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/4983288e-00e5-4ac5-a008-c757c88d5dc2)

## Introduction
In this article, I'll show you how to display the map in the image above. It might look intimidating, but it's really not! In fact, it only takes a couple lines of code.

## Importing the Libraries 
There are **4 visualization libraries needed** for this to work:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/f62f04f8-d668-465f-b965-73b367483b63)

If you forget to import one of these libraries, you will run into an error since **the map won't render properly**. 

## Loading the Data
Now, we're going to load our data with the help of the GeoPandas library. It has a method called **.read_file** where you pass in the **file path**.

I'm going to use a dataset on Chicago's crime, health, and population stats in 2014. You can download it here: https://geodacenter.github.io/data-and-lab/comarea_vars/.

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/839eb7ce-7bd8-4798-8112-d04a4f33c960)
(Thanks to https://unsplash.com/@sawyerbengtson on Unsplash)

Here's what the code looks like:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/4a50f619-d806-425d-a105-061831bb9f5c)

Doing this will make "file" a **GeoDataFrame**, which means we're closer to getting our final map. 

## Peeking at the Data
I just want to look at the **first 5 rows** of this GeoDataFrame. All I have to do is call the **.head** method:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/9d9d52ae-92cf-440d-b1fb-162bf142cba9)

If you scroll all the way to FINISH THIS LATER
