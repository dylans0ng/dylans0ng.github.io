# 3 Main Steps when doing a SQL project

<p align="center">
  <img width="550" height="500" src="https://user-images.githubusercontent.com/112503726/200104695-41053259-3ef2-4dcd-976f-0ab0f1f043da.png">
</p>

## Introduction
After doing a few SQL projects in the past, I realized that there is a pattern, or cycle if you will, when doing these kinds of projects. I wanna share this to anyone interested in data science because it is crucial to understand how to approach a project if you want to improve your data analytical skills. 

I broke this pattern up into 3 broad categories and came up with a nice three letter acronym for it: **ACE**.

## ACE

**A**SK QUESTIONS
<p align="center">
  <img width="250" height="200" src="https://user-images.githubusercontent.com/112503726/200105083-c3b7f364-ad19-4add-accc-1fce445dfe34.png">
</p>

  - If you want to learn and gain insights from a dataset, it is important that you ask questions. 
  - By asking yourself questions, you are creating a mental plan of what you want to do with the data.
  - Not asking any questions will not get you anywhere because you will just be staring blankly at the data without any goal in mind.
  
**C**LEAN DATA
<p align="center">
  <img width="350" height="280" src="https://user-images.githubusercontent.com/112503726/200105125-b7236ee0-7e12-4afe-b855-bd3209e10e68.png">
</p>


  - 99% of the time the data for your project will be messy. What I mean by "messy" is that there could be many **missing entries**, **null values**, and data that is in an **incorrect format**. 
      - For example, if you have a column of strings that contain all the number of customers a specific product has received, it is important to **change the data type** of the values to an integer in order to perform meanginful functions
  - It is beneficial to remove any unncessary columns that **do not answer your questions**. If you have a specific goal that you want to achieve with the data, there's no point in keeping a column with data that is completely irrelevant. 
  - Once you're done cleaning the data, you're ready to analyze the data and come up with meaningful insights. 

**E**XPLORE DATA
<p align="center">
  <img width="350" height="290" src="https://user-images.githubusercontent.com/112503726/202106836-a24bdef5-e1ed-4a7c-ae85-894c2e2f92b6.png">
</p>

  - Once you clean your data, you can now dive into the data and try to think of some SQL functions to use to answer your statistical question. 
       - For example, if one of your questions was "What is the **average sales price** of the products sold", then you would have to use the **AVG() function**.
  - While it is okay to run queries via trial and error, it is good practice to try and **come up with a plan** on how to create the query that answers your question and then type it all out on the first try. As you **practice SQL more**, you will naturally be able to think and code out the query more efficiently.
  -  After you run your query, you can make analyses from the results and come up with your own conclusions of the data.
  -  To take it a step further, you can use **BI tools such as Power BI** to visualize your data. After all, it's much easier to gain insights from visuals than from tables of numbers. 

## Conclusion
Thank you for reading this post! I hope you found it helpful. If there's anything else you think is important when doing a SQL project, please drop it down in the comments below! 
