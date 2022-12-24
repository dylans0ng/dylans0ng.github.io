# Optimization using Calculus
![image](https://user-images.githubusercontent.com/112503726/209005707-c1cb7716-818b-4c74-add5-11a29233f667.png)

## Introduction
Hello everyone, how are you all doing? In this post, I'm going to be going over one of the most important concepts in calculus: **optimization**. It's very useful because **optimization can be applied to many different real-life scenarios**.

For example, let's say you are the owner of a business and you want to **maximize the profit** that you make based on all the products you sell. Well to do this, you would have to use calculus! By the end of this post, you are going to know how to solve this kind of problem.

Not only are we going to learn how to find the maximum profit, but we will also learn how to find the **minimum cost**, the **maximum/minimum area**, the **maximum/minimum volume**, and much more! So whether you are studying for a test or you are just curious about what optimization is, then keep reading!

## Optimization: A Brief Overview
### What is Optimization?
Optimization is all about finding the **GLOBAL EXTREMA**. Global extrema refers to **global minimum** and **global maximum**. 

### Global Extrema

**Global minimum** = Lowest value in the function. 

**Global maximum** = Highest value in the function. 

![image](https://user-images.githubusercontent.com/112503726/209007039-6562b618-fc81-455f-8a29-a5d86704bb3d.png)

Keep in mind that global extrema represents the value of f(x), **NOT the x-value**. 

So, for example, you would say, "The function f(x) has a global minimum of 5 **AT X = 2**". You would **NOT** say "The function f(x) has a global minimum of 2".

### The EXTREME VALUE Theorem
If f is **continuous** on the closed interval a <= x <= b, then f has a **global maximum** and **globam minimum** on that interval. 

## Finding Global Extrema
### Critical Points using First Derivative 
In order to find global extrema, you must know how to find **critical points**. Critical points are where the **slope of the tangent line** is 0 OR undefined. 

To find the specific x-values of the critical points, we must find the first derivative of the function, **set it equal to 0**, and solve for x. We must ALSO **find x-values that make the first derivative undefined**.

#### EXAMPLE
![image](https://user-images.githubusercontent.com/112503726/209275495-8d6e4340-4368-4a02-9235-b9c99550d0f2.png)
![image](https://user-images.githubusercontent.com/112503726/209275536-c6a5d976-cfcb-470c-bc2e-8ea66dfb8eee.png)

To solve this problem, I first found the first derivative and set it equal to 0. Notice that **I don't have to worry about finding x-values that are undefined** because the first derivative is a **quadratic that will never be undefined**.

Now that you understand how to find critical points, you must use those points to find the **global extrema**.

### Testing the Critical Points
To find the **global extrema**, we must TEST the critical points. 

#### Look at the ENDPOINTS of the domain interval 
When you are given a question that asks you to find the global min and max of a function **within a closed interval**, then here's what you do:
1) Find the critical points of the function by setting the first derivative **equal to 0** and finding x-values where the derivative is undefined (if necessary).
2) Plug in the critical points AND the **endpoints of the closed interval** into the **original function**, NOT the derivative of the function.
3) See which x-value will produce the smallest and greatest values. These values are your **global min and max**.

Here's the 3 step process in action:
#### Closed Interval Example
Find the global min and max for the function on the closed interval:
![image](https://user-images.githubusercontent.com/112503726/209277409-344e4f96-7433-4d48-9eca-3e7f25aa66fe.png)
![image](https://user-images.githubusercontent.com/112503726/209277702-59420c33-cdea-4d0e-85a7-bbfc1531cccc.png)

Now, let's look at some tougher problems. 

## Optimization Word Problems
Here's where the fun begins. Often times, in your calculus class, the questions won't be as easy as the examples that I had above. You're going to have to look at long word problems that require you to either **minimize or maximize** a certain thing.

Anyways without furtherado, let's dive right into it, and I'm warning you that these problems are gonna be pretty hard. So, if you're up for the challenge, read on! 

![image](https://user-images.githubusercontent.com/112503726/209278662-c955a3f3-9576-48d6-8b6d-075fd9161a6d.png)
Caption: Don't be scared, you'll be fine 😀!

Here is the process of dealing with optimization word problems:
1) If the question deals with anything related to volume or area, **DRAW A PICTURE** (if the problem doesn't give you a diagram)
2) Label the picture with **convenient variables** such as x, y, or h
3) Write a **"primary" formula** for the quantity that needs to be maximized or minimized. Common primary formulas include area = length * width, volume of cylinder = pi(radius * radius)(height), volume of rectangle = length * width * height
4) Reduce the "primary" formula that you created so that it only has **one variable**
5) Create practical endpoints of this one variable. This is essentially your **domain interval**. This step requires you to analyze the **context of the scenario**, so you must not only understand what the question is asking you, **but you must also understand the context of the question**.
6) Find the critical points of the function (this is why critical points are important). Find the global max or min (recall how we did this in the previous section).
7) Answer the question **IN CONTEXT** and draw a box around it to tell the person grading your paper that is is your **final answer**.

So, here are some big word problems using this process in action. For any of these problems, **try to do the problems yourself BEFORE looking at my answer**. If you try the problem yourself but can't solve it, THEN you can look at the answer.

### Cutting a Box
![image](https://user-images.githubusercontent.com/112503726/209280192-a9139212-737d-47ab-9531-f4c888a38671.png)

Answer:

![image](https://user-images.githubusercontent.com/112503726/209419548-59cb87ca-a877-4437-89ad-130147f81bef.png)
![image](https://user-images.githubusercontent.com/112503726/209419655-b290ce97-eea7-47b5-ba3a-3bcc07132a02.png)

We can set up a formula as a function of "x". 

![image](https://user-images.githubusercontent.com/112503726/209419693-a7a91d45-8337-454a-842d-3c73f6500000.png)

This is our domain. Our x-value can't be less than 0 because you can't have a side length that is negative. Our x-value can't be greater than 4 because then our width, which we represented as 8-2x, will become a negative value, and that's not possible.

![image](https://user-images.githubusercontent.com/112503726/209419845-6c74e795-0470-44cc-be14-b86f334e52dd.png)

Remember when we find critical points, we must **eliminate** any critical points that are **OUTSIDE OF OUR DOMAIN THAT WE CREATED** (this is why creating the domain is important!). 

![image](https://user-images.githubusercontent.com/112503726/209420062-b735dc3c-09cb-4a2a-844f-448b3346d6f6.png)

Now, you plug in the critical points AND THE ENDPOINTS OF THE DOMAIN into your **original function**, NOT the derivative. 

You can see that when x is about 1.569, then the volume of the cut box is **maximized**.

But, we're not done yet. We gotta answer the question.

![image](https://user-images.githubusercontent.com/112503726/209420184-89563814-470f-48f8-95f6-a9bc1d8d15f8.png)

You MUST answer the question in the end. Do NOT forget the units in the problem. 

Okay, let's move on to a trickier problem...

### Polygon Inscribed Inside Another Figure
![image](https://user-images.githubusercontent.com/112503726/209420257-b7d28f83-2542-48f8-b9d5-299f89978403.png)


FINISH THIS PROBLEM LATER!


## Conclusion
### Resources that I've used
Professor Leonard's videos are amazing. 
