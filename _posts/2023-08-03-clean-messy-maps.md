# Clean Up your MESSY MAPS in Python
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/c991a5c2-bba3-47b3-8dd9-a69512190ab9)

## Introduction
In the map above, there are **too many columns showing up** when I hover over one of the polygons.  In this article, you'll learn how to **remove the columns that you don't want** and **keep the ones that you do want** in the dataframe. 

This is a **part 2** article; if you haven't already, check out my [part 1](https://medium.com/data-and-beyond/how-to-create-interactive-maps-in-python-983e01979201) article, where I show you step-by-step how to create the map! 

## Specifying Certain Columns
Let's say that I want to only see **3 of the columns** when I hover over the polygons: "community", "Pop2014", "Property_C". To do this, I can do this:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/1c11176c-87a4-44fc-af21-1368779bb3cd)

I'm keeping the "**geometry**" column because **I need the coordinates** to be able to create a map from the data. 

This will get a dataframe called "**file**" that only shows the columns that we want:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/576a3a65-09ef-4918-b50d-4d6d3ccd85fc)

## Displaying the Updated Map
Now we can display the map again on the **property crime rates in Chicago**:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/857cbb6e-4fcd-44f7-894c-0c1e03cf1a37)

And if I hover over the polygon, it's a lot cleaner:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/b1713a8c-d8b1-4997-98f4-c1eee9b0cc44)

## Renaming the Columns
However, **there's still a problem**.

If you haven't looked at the dataset description, you might not know what "Pop2014" or "Property_C" means. I'm going to **change the column names** so that they make more sense to everyone. 

Here's the code for this:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/2e7d83fc-f8f3-4aaa-86bf-dd62b303c8d4)

Inside the **.rename** method, you can see that I passed in a **dictionary**. Each key in the dictionary represents **the ORIGINAL column name**, and each value represents **the NEW column name** for its corresponding key. 

So, **in this example**, I change "community" to "Neighborhood"; "Pop2014" to "Population in 2014"; and "Property_C" to "Property Crime".

Here's what the dataframe should look like now:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/43e0cda7-ec61-43e9-9333-1f52bbaac61f)

## Displaying the Updated Map WITH THE RENAMED COLUMNS
Now, let's display the map with our **updated dataframe**:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/0c590322-78d2-4a7d-bb37-ac251c2d7251)

Notice that I said "Property Crime" instead of "Property_C". This is because we changed the column, so **"Property_C" no longer exists**. If you tried to pass in "Property_C", you **would get an error**.

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/a1776990-0db7-49bb-b2d0-176b1e17e6c2)

Looking at the map, all of our 3 columns are changed and that looks really clean! 

## Video Explanation
Thank you for making it all the way here! I've made a YouTube tutorial that **goes over the steps** that I talked about in this post. Feel free to check that out here: (insert video)
