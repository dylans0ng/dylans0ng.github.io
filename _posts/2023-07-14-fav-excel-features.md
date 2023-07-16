# My Favorite Excel Feature: VBA! 
## Introduction
I love Excel because of its simplicity and its ability to **efficiently organize data**. In this post, I'm going to share my **FAVORITE feature in Excel** that every data analyst should use.

## What is VBA?
VBA stands for **Visual Basic for Applications**, and it's available in all the Microsoft Office apps. It allows you to write code that'll **automate repetitive tasks** and save time. 

This is perfect for data analysts because they can implement VBA code to accomplish tasks such as easily formatting multiple workbooks with **a single button press** instead of manually changing each one. 

The good news is, if you have **previous programming knowledge**, learning VBA will be a lot easier since many of the concepts **translate to other languages** like Python or Java. 

## Where do I type the VBA Code?
If you open up Excel and do **Alt + F11**, a new pop-up window will appear:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/c9b38757-7a9b-4657-88b1-6fcbb2f7426f)

This is called the **VBA Editor**, or VBA Interface, and you'll be able to enter in code in the macros that you create. 

## What are macros?
Inside a macro, you can enter **sequences of VBA code statements** where you put in your VBA code. 

To create a macro in the VBA interface, click on the "Insert" ribbon:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/77f8f577-c2a9-4d2b-b2d5-0d602c2c2179)

Then, click on "Module". Once you do that, you should see white space that looks like this:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/efa121ac-e599-4f45-8335-e304190960b7)

## What are procedures?
If you have previous coding knowledge, think of **procedures** as **functions**. A procedure contains some VBA code that you can **call anytime**. 

For example, here's a procedure that'll automatically insert headers:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/f4c7b658-9655-4b70-8177-4a6dbf1af09b)

It's ok if the code doesn't make sense! Basically, I **inserted column names** and made sure that they were on the **first row of the data**.

If I want to call this procedure called "**InsertHeaders**", then I'll go back to the Excel interface and go to the "**Developer**" ribbon:
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/a0c9155d-7413-4799-9218-ab0295f90eff)

From there, click on "**Macros**":
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/dcaa505a-8258-46f8-ab59-fa665b37b97f)

Then, you can select the "InsertHeaders" procedure and click "**Run**" (ignore the other procedures I've made):
![image](https://github.com/dylans0ng/dylans0ng.github.io/assets/112503726/f6f98dd2-2565-4e5a-9a12-a56fa71468e2)

## More Excel VBA Concepts 
Because Excel VBA is a broad language, there's so many more concepts to learn about! You should check out this website which explains each of the different VBA components. 
