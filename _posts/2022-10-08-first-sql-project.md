# My First SQL Project: Data Science Salaries 

## Introduction
Hello everyone! This is my first SQL project on Postgres and I want to share this because it might be helpful for those of you that are learning the basics of SQL. I hope you read until the end to see what I accomplished!

## Project Topic
This project is about the salaries of different data science positions and I got the [dataset](https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries) from Kaggle. If you want to play with the dataset yourself, I encourage you to check it out! 

## Statistical Questions
When doing a project, it is always important to have a goal in mind. That is why I created some questions to answer as I build queries:
- What are the top 10 average salaries for the different data science job positions?
- Does being employed full-time make your salary higher?
- How does job experience level impact your salary?
- How does the size of the company impact your salary?

## The Data
_DISCLAIMER: Whenever I show snips, I will only show the first 10 rows of the data because I cannot show 3000+ rows in a single image._

Here is an image of the original dataset:
![image](https://user-images.githubusercontent.com/112503726/194731820-b539d123-d531-492b-9978-84d415e38b96.png)

We can see that there are 11 columns:
- work_year 
- experience_level 
- employment_type
- job_title
- salary 
- salary_currency
- salary_in_usd
- employee_residence
- remote_ratio
- company_location
- company_size

First, I created all the column headers before I imported the data.
```tsql
CREATE TABLE Public."ds_salaries"(
    work_year SMALLINT NOT NULL,
    experience_level VARCHAR(5) NOT NULL,
    employment_type VARCHAR(5) NOT NULL,
    job_title VARCHAR(200) NOT NULL,
    salary INTEGER NOT NULL CHECK(salary > 0),
    salary_currency VARCHAR(30) NOT NULL,
    salary_in_usd INTEGER NOT NULL CHECK(salary_in_usd > 0),
    employee_residence VARCHAR(5) NOT NULL,
    remote_ratio SMALLINT NOT NULL,
    company_location VARCHAR(5) NOT NULL,
    company_size VARCHAR(2) NOT NULL
)
```
Then, I imported the data from a csv file called "ds_salaries" using the **COPY WITH** statement.
```tsql
COPY ds_salaries
FROM 'C:\mydirectory\ds_salaries.csv'
WITH (FORMAT CSV, HEADER);
```

And voila! I successfully imported the data from Excel into pgadmin!
```tsql
SELECT * FROM ds_salaries;
```
![image](https://user-images.githubusercontent.com/112503726/195971218-13f4af03-f007-480e-b025-52e957bf6e75.png)
Now, I can finally start cleaning the data inside Postgres.

## Data Cleaning Time
There is a lot of cleaning to do inside this dataset. There are many unnecessary columns that should be removed. After all, what's the point of keeping a column if it's not going to help me answer my statistical questions? 

### Deciding which columns to remove
If you look at my [statistical questions](#statistical-questions), the main things I need are the job title, employment type, experience level, company size, and salary. 

However, if you take a closer look at the original [data](#the-data) in Excel, there are two columns that relate to salary: "salary" and "salary_in_usd". Now, I'm in the US, so I'm just going to keep the "salary_in_usd" because USD is the standard currency in America. So, that means I'm going to get rid of the "salary" column as well as _all the other columns_ that don't pertain to my statistical questions.

```tsql
ALTER TABLE ds_salaries
DROP COLUMN work_year, 
DROP COLUMN salary, 
DROP COLUMN salary_currency, 
DROP COLUMN employee_residence, 
DROP COLUMN remote_ratio, 
DROP COLUMN company_location;
```
Now, the data is a lot better because it only includes the info that I need to answer my statistical questions:
![image](https://user-images.githubusercontent.com/112503726/196012787-56c55b2f-37c8-435f-a32d-67d8e1af7ad0.png)

## Statistical Question 1: What are the top 10 average salaries for the different data science job positions?
```tsql
SELECT job_title, ROUND(AVG(salary_in_usd), 2) AS Salary_in_USD
FROM ds_salaries
GROUP BY job_title
ORDER BY salary_in_usd DESC
LIMIT 10;
```
I used a simple **GROUP BY** statement to get the average salaries based on the job titles and used **ORDER BY** and **LIMIT** to grab only the top 10 average salaries.
![image](https://user-images.githubusercontent.com/112503726/196013235-70b9c410-a62d-4228-8753-5f9a9ad98d8b.png)

Based on the result, the best paid position is "Data Analystics Lead" with a whopping average salary of $405,000! Managers tend to make more money in a company because they lead the whole team, so it makes sense that the highest paying job is a position that requires good leadership skills.

## Statistical Question 2: Does being employed full-time make your salary higher?
This statistical question requires the column called "employment_type". Here is a legend of what the values in "employment_type" mean:
- PT = Part time
- FL = Freelance
- FT = Full time
- CT = Contract
```tsql
SELECT employment_type, ROUND(AVG(salary_in_usd), 2) AS average_salary_in_usd
FROM ds_salaries
GROUP BY employment_type
ORDER BY ROUND(AVG(salary_in_usd), 2) DESC;
```

Result:

![image](https://user-images.githubusercontent.com/112503726/196013578-921d0af4-d5b6-4c0d-8064-ff97a65b90c4.png)

I thought that people working full-time would make the most, so I was surprised when I saw that contractors made more than full-time employees. Then, I realized that contractors can make more money since they do not receive any benefits while full-time employees usually receive benefits such as medical benefits. 

So, to answer my statistical question, full-time employees typically get paid more compared to part-time workers but make less than contractors.

## Statistical Question 3:
