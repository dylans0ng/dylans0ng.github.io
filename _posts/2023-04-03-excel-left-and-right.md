# LEFT() and RIGHT() Function
![image](https://user-images.githubusercontent.com/112503726/229691444-5ff081ca-d045-4727-85f7-f1bb73ccc8a9.png)
![image](https://user-images.githubusercontent.com/112503726/229691457-3bae7315-39d7-444a-9348-d4ad8afc0beb.png)


## Introduction
Hi everyone! I haven't posted in a while as I've been busy with school, but I'll try my best to post more often from here on out. In this post, I'll explain what the **LEFT() and RIGHT()** functions are. They are very easy to use and can be useful if you want to **split up a text** into a separate cell. 

## LEFT()
The LEFT() function returns the number of characters from **the left side** of the text.

Consider this example:

![image](https://user-images.githubusercontent.com/112503726/229337162-0b3e7cc7-f18f-4e97-8e57-75b94a45ba98.png)

Let's say I want to get my first name.

I know I can just type in "Dylan". But, **we shouldn't do things manually** because if we get a big dataset with hundreds of names, it's gonna be **hard to manually type every single first name** in. Luckily, we can use the LEFT() function.

Here's the syntax:
LEFT(**text**, **num_chars**)

"**text**" represents the text value. 

"**num_chars**" represents the number of characaters from the left of the string. 

So, since my first name is 5 characters long, we can do this:
![image](https://user-images.githubusercontent.com/112503726/229337352-5290e0d6-c3e8-4c5f-aa2f-ad18785eba01.png)

... and bam! We got the first name:
![image](https://user-images.githubusercontent.com/112503726/229337361-79dcaa41-bc9f-4120-a5a4-755ba6774860.png)

## RIGHT()
The RIGHT() function works the EXACT same way as LEFT(), but this time, it returns the number of characters from **the right side** of the text instead of the left.

The syntax is the same: RIGHT(**text**, **num_chars**)

I could use this function to get my **last name**. Because my last name is 4 characters long, we can do this:

![image](https://user-images.githubusercontent.com/112503726/229691577-caf65e33-4987-41b3-b268-1c1f77eb072a.png)

This will get the **last 4 characters** of the text, which is "Song":

![image](https://user-images.githubusercontent.com/112503726/229691647-dae8ba19-c166-445e-9a9f-4a40c5078d38.png)

It's that simple!

## Conclusion
Thank you for reading and I hope this was helpful! In my next post, I'll talk about a tool that you should use that will help you write any Excel formula, so stay tuned for that! 
