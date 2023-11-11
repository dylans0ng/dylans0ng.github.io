# Web Scraping Wikipedia Data Using Pandas [3 Steps]
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/1e80cb82-0d01-467b-8bc9-edb494e38115)

## Introduction
In this blog post, I'll show you how to **web scrape any data from Wikipedia** in Python. It's really easy to do and only requires **3 steps**! So, without wasting any more time, let's jump into it...

## Step 1: Import Libraries
First, you have to import the **Pandas** library:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/e4039ebf-327d-4d5c-ad8d-a5ce573f50d4)

Then, import the SSL library:

![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/3084252c-567d-49b5-b71d-760e4a38f54b)

It's important to include the **last line of code** or else you **might get an error** saying that the certificate verification failed. 

After you import both these libraries, you're ready to move on to the next step...

## Step 2: Use the Read_html Method
The read_html method is provided by the Pandas library and will automatically **convert HTML tables into Pandas dataframes**, making it easy for us to analyze the web data in Python. It requires **one argument** - the link of the website.

So, all you gotta do is **create a new variable**:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/019d9bc1-bdcd-4b68-9f1f-311935b3b1e0)

In the code above, I created a new variable called "**tables**" and set it equal to the read_html method, with the **Wikipedia article link as the argument**. This means that "tables" will contain **all data contained in an HTML table** from the Wikipedia article.

However, we're still not done yet. There's one more thing to do...

## Step 3: DO THIS LATER

TALK ABOUT WHAT TO ACTUALLY TYPE INSIDE THE PYTHON EDITOR!!!

BASICALLY JUST LOOK AT THE "WEB SCRAPING WIKIPEDIA DATA" PAGE IN ONENOTE
