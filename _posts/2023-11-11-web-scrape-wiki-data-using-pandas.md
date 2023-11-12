# Web Scraping Wikipedia Data Using Pandas [3 Steps]
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/1e80cb82-0d01-467b-8bc9-edb494e38115)

## Introduction
In this blog post, I'll show you how to **web scrape any data from Wikipedia** in Python. It's really easy to do and only requires **3 steps**! So, without wasting any more time, let's jump into it...

## Step 1: Import Libraries
First, you have to import the **Pandas** library:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/e4039ebf-327d-4d5c-ad8d-a5ce573f50d4)

Then, import the **SSL** library:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/3084252c-567d-49b5-b71d-760e4a38f54b)

It's important to include the **last line of code** or else you **might get an error** saying that the certificate verification failed. 

After you import both these libraries, you're ready to move on to the next step...

## Step 2: Use the Read_html Method
The **read_html method** is provided by the Pandas library and will automatically **convert HTML tables into Pandas dataframes**, making it easy for us to analyze the web data in Python. It requires **one argument** - the link of the website.

So, all you gotta do is **create a new variable**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/019d9bc1-bdcd-4b68-9f1f-311935b3b1e0)

In the code above, I created a new variable called "**tables**" and set it equal to the read_html method, with the **Wikipedia article link as the argument**. This means that "tables" will contain **all data contained in an HTML table** from the Wikipedia article.

However, we're still not done yet. There's one more thing to do...

## Step 3: Check Which Table to Use
Depending on how big the article is, you might get **multiple data tables** when you scrape the website. Take a look at this, for example:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/5cbefb79-2b31-4d13-a05c-b4045efd388d)

Since my Wikipedia article is pretty big, there are **4 HTML tables** that Pandas automatically scraped. So, I need to find **which data table has the correct information** that I'm interested in - video game sales.

So, this will take some **trial and error**. You have to use **indexing** to find the table that you want:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/37a0cc7e-6c95-4512-bf7a-a383952f46cd)

I obtained the **first table** within "tables" by putting a 0 inside the square brackets. Remember, Python uses **zero-based indexing**! 

The first table doesn't look like the one I want because it doesn't include the video game sales. So, I'm gonna do the same thing, but this time I'll get the **second table**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/fc91dc24-d22f-493e-95ee-3fde3dd5c906)

This looks like the right one because it contains data on all the video game sales. 

Once you **find the data table** that you want, you can save it into a **new variable**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/37d9ddd7-084b-452a-939b-cd70046f04bd)

Now, you can **conveniently refer to this new variable** when you do your analysis.

## Video on Web Scraping Wikipedia Data
Ok that's all I got for this post! Hopefully, you found it helpful, but if there's something that still doesn't make sense, then I encourage you to check out a **short 2-minute video** that I made: https://youtu.be/0FKOugdhExw

It'll give you a more clear explanation on **how to web scrape Wikipedia data**. I hope to see you there, and thanks for reading! 
