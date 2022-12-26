# Optimization using Calculus
![image](https://user-images.githubusercontent.com/112503726/209005707-c1cb7716-818b-4c74-add5-11a29233f667.png)

## Introduction
Hello everyone, how are you all doing? Just a heads-up: this post is gonna be pretty long! So, I recommend that you use the **table of contents** to jump to a specific part that you wanna look at. Anyways, in this post, I'm going to be going over one of the most important concepts in calculus: **optimization**. It's very useful because **optimization can be applied to many different real-life scenarios**.

For example, let's say you are the owner of a business and you want to **minimize your costs** because you don't want to spend too much. Well to do this, you would have to use calculus! By the end of this post, you are going to know how to solve this kind of problem.

Not only are you going to learn how to find the minimal cost but you will also learn how to find the **maximum/minimum area** and the **maximum/minimum volume** based on the context of a problem! So whether you are studying for a test or you are just curious about what optimization is, then keep reading!

## Optimization: A Brief Overview
### What is Optimization?
Optimization is all about finding the **GLOBAL EXTREMA**. Global extrema refers to **global minimum** and **global maximum**. 

### Global Extrema

**Global minimum** = Lowest value within the domain of the function. 

**Global maximum** = Highest value within the domain of the function. 

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

**Answer:**

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

**Answer:**

Based on the information given, you can draw this diagram:
![image](https://user-images.githubusercontent.com/112503726/209420949-6d5d4b57-19f1-4775-9445-e9c40d5c8a82.png)

You might be wondering what the point was to draw the diagonal inside the rectangle. Well, what we drew inside the rectangle was a **right triangle**, so we can use the **Pythagorean Theorem** to solve for one of the variables. 
![image](https://user-images.githubusercontent.com/112503726/209421025-c0b7a7ff-a93b-42e1-b99e-48bed872a954.png)

![image](https://user-images.githubusercontent.com/112503726/209421065-20372bde-d474-4ea6-bac8-95fcd69fc5df.png)

This is our primary equation. Since we solved for "w" already, we can **substitute our equation for "w"** and plug it into our primary equation so that the formula is a function of "L".
![image](https://user-images.githubusercontent.com/112503726/209421114-c05791e7-232d-4ba0-b5b8-fe834634c32e.png)

Now, we gotta set our **domain**. We know that L cannot be less than 0 because a side length **cannot be negative**. Also, if L is greater than 2, then "w" will become negative, which is not possible. So here's our domain:
![image](https://user-images.githubusercontent.com/112503726/209421149-930fb314-526d-4eb1-8f73-72c8350ef6c4.png)

Now, we must find the derivative of the function we created by using the **chain rule** and **product rule**.
![image](https://user-images.githubusercontent.com/112503726/209421189-1460dec8-6d24-4cea-b40e-224ff1bb35d4.png)

After we get our derivative, we need to find the critical points **within our domain that we made**.
![image](https://user-images.githubusercontent.com/112503726/209421218-a419d1a2-d362-4c50-b400-0570615836af.png)

Plug in critical points and endpoints:
![image](https://user-images.githubusercontent.com/112503726/209421251-15f6d3f5-6ac5-475c-9f17-8470ff8859d2.png)

Answer the question: 
![image](https://user-images.githubusercontent.com/112503726/209421272-c1a881fd-6c99-4585-a2c5-72958343f2a0.png)

I hope you are seeing a **pattern** in these questions because once you get a lot of practice of optimization problems, they will get a lot easier!

### Minimal Path
![image](https://user-images.githubusercontent.com/112503726/209500314-67f5c742-751b-4466-bda9-467e35c95c90.png)

This problem looks very confusing, but luckily, they give us a diagram:
![image](https://user-images.githubusercontent.com/112503726/209500440-b2a25696-9c93-4029-a305-81b248217bd5.png)

**Answer:**
First, we should label the diagram:
![image](https://user-images.githubusercontent.com/112503726/209500560-120ebef5-503b-49c1-bb22-eeeaa18ef5e0.png)

Basically, we need to find the **minimal length** of the part that I have highlighted in yellow. I've used the Pythagorean theorem to get the hypotenuses (the blue and red part). 

Now, we can create an equation as a **function of x**. I'm gonna call the function D(x) to represent the length of the pipe:
![image](https://user-images.githubusercontent.com/112503726/209500706-16fda29f-e9c2-43fa-8937-9e09c9457be2.png)

Notice that I've changed the formula so that I can **easily apply the chain rule it** since we're going to have to take the derivative later.

Let's create a domain for **x** now. We know that x can't be less than 0 because it's impossible to have a negative length. Also, if you look at the diagram, you can see that x can't be greater than 4. So, here's our domain:
![image](https://user-images.githubusercontent.com/112503726/209501590-bfd44464-5b38-4f57-afdb-5d181296b019.png)

Take the derivative of the function using **chain rule**:
![image](https://user-images.githubusercontent.com/112503726/209513537-b37c0505-2cf3-4af2-bbd3-5d2654beb25d.png)

The derivative looks pretty complicated, but don't let that stop you. Just keep going along with the process!
![image](https://user-images.githubusercontent.com/112503726/209513589-9a190520-b29c-4621-b824-2aa74b95306a.png)

So, our only critical point **that is within our domain** is 0.8. You gotta find the **global minimum** now:
![image](https://user-images.githubusercontent.com/112503726/209513915-e8bd2e09-b351-4253-b572-ce3c9b014f6f.png)

I plugged in the **endpoints** and the **critical point** into the ORIGINAL function that I created. When x = 0.8, the length is the smallest, so that is our **minimal length**.

Final answer:
![image](https://user-images.githubusercontent.com/112503726/209514080-c5575c50-3987-42a4-854c-72dc40309f2f.png)

Don't forget to include **UNITS** in the context of the problem!

### Minimal Cost
![image](https://user-images.githubusercontent.com/112503726/209514597-ad5fb28e-800f-4510-8bb5-eca9998dc0ec.png)
(Credit to Khan Academy)

**Answer:**
Draw a picture:
![image](https://user-images.githubusercontent.com/112503726/209514779-29f516fa-971a-4f66-94bb-cd0167c58551.png)

The question also gives us info on the length and width, so let's list what we know here:
![image](https://user-images.githubusercontent.com/112503726/209514984-a9a8556f-9e7d-48a9-b4d9-657753bdbc26.png)

Now, you can solve for one of the variables. I'll solve for "h", but you can solve for "w" if you want and you'll still get the right answer.
![image](https://user-images.githubusercontent.com/112503726/209515104-cd319b9f-f29d-4bf7-aea5-cf9a353a98e0.png)

Based on the question, the cost depends on the **surface area** of the box. Also, notice that the question says that the box has an **OPEN** top. This will affect our surface area because we **cannot include the area of the top part** of the box. Here's our surface area equation:
![image](https://user-images.githubusercontent.com/112503726/209515299-f71fa2cb-7f97-42c7-b6ab-03be732a61a1.png)

You can see that I basically **replaced L with 2w** since we know that the length is 2 times the width.

Now, you come up with our cost equation:
![image](https://user-images.githubusercontent.com/112503726/209515972-726ee405-e1cc-4c81-a2ba-94369be0cc08.png)

You can write the cost equation as a function of a single variable "w". All I'm gonna do is replace **h with 5/w^2**:
![image](https://user-images.githubusercontent.com/112503726/209516165-5a9117f2-a112-4bb9-9a0e-d7dda3d83e63.png)

"w" has to be greater than 0 because you can't have a negative width and if "w" is 0, then "h" will become undefined. At the same time, "w" also can't be greater than 10 because **a single side of a prism can't be greater than its own volume**. So, this is our domain for "w":
![image](https://user-images.githubusercontent.com/112503726/209516356-287bfff3-cab6-4ceb-94cf-2121a935801c.png)

Take the derivative of C(w) by using the **power rule**:
![image](https://user-images.githubusercontent.com/112503726/209575046-81c77a6c-8c66-47fd-a231-698730f4772f.png)

Find critical points:
![image](https://user-images.githubusercontent.com/112503726/209575179-201eb33c-06ee-440f-bda2-0c22aba8bcd9.png)

Find **global minimum**:
![image](https://user-images.githubusercontent.com/112503726/209575203-6ba8e3b2-c16d-48e5-b6c1-3861ee3f740b.png)

Answer the question: 
![image](https://user-images.githubusercontent.com/112503726/209575237-aa072f0f-5347-45e7-8828-fa44ab5d7ec4.png)

## Conclusion
If you've gotten all the way here, I wanna congratulate you for reading this long post all the way through! This post provided examples of different kinds of optimization problems. I hope you got a better understanding of optimization using calculus; if not, here are a list of resources that you can use to get more practice!

### Resources that I've used
Professor Leonard video: https://www.youtube.com/watch?v=SWZcq_biZLw&t=2317s
Khan Academy: https://www.khanacademy.org/math/ap-calculus-ab/ab-diff-analytical-applications-new

That's it for this post! I hope you have a good day and thank you for reading!

