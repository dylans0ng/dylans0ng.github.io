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

If you keep scrolling through the dataset, you'll notice that the last column says "**geometry**":

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/424cf3b9-fda1-4503-9391-a551d750f850)

This column has a bunch of **Polygon objects** that contain coordinate points. These Polygons allow Python to create a map from the data, and every GeoDataFrame **must have this column**.

## Creating the Final Map
We only have two lines of code left! The nice thing is that the GeoPandas library provides us with **.explore**. In this simple method, we just have to pass in the column name(s).

I want to see how the property crime rates differ across the different Chicago areas, so I'm gonna say this:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/0ce07b08-948e-4456-b56f-3e2bffd3abd7)

In this case, "**Property_C**" is the column name in the dataset. But you can put in whatever column you want since you're the analyst!

Here's what the final result looks like:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/d474b244-0009-45d7-91ef-694458feae34)

The cool thing is that you can **move the map around** and **zoom in/out**. I encourage you to try it yourself! 

## Video Explanation
Thank you so much for reading this article! If you want to see me walk through all the steps that I just talked about, then feel free to check out this video: PLACEHOLDER.

It'll only take 3 minutes of your time 😀
