# My First SQL Project: Data Science Salaries 

## Introduction
Hello everyone! This is my first SQL project on Postgres and I want to share this because it might be helpful for those of you that are learning the basics of SQL. I hope you read until the end to see what I accomplished!

## Project Topic
This project is about the salaries of different data science positions and I got the [dataset](https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries) from Kaggle. If you want to play with the dataset yourself, I encourage you to check it out! 

## Statistical Questions
When doing a project, it is always important to have a goal in mind. That is why I created some questions to answer as I build queries:
- What is the average salary for the different data science job positions?
- Does being employed full-time make your salary higher?
- How does job experience level impact your salary?

## Creating the table 
``tsql
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
``tsql



 
