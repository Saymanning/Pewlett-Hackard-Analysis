# Pewlett-Hackard-Analysis

## Overview

### Purpose of Analysis
The purpose of this analysis was to determine the number of employees retiring from Pewlett Hackard by job title and to identify employees who are eligible to participate in a mentorship program. A written report was also provided to help the manager prepare for the upcoming "silver tsunami" as many employees reach retirement age.

### Results 

**Retiring Employees by Title**

- The first step was to retrieve the number of employees retiring from Pewlett Hackard and also include their job title. The employee number, first name and last name were       retrieved from the columns in the the Employees table.
- Then the employee title, "from date" and "to date" were retrieved from the Titles table.
- A new table was created using the primary key and the date was then filtered on the birth date column to retrieve employees born between 1952 and 1955 and ordered by the       employee number. See images below.

Query:

<img width="351" alt="Retirement_Titles code" src="https://user-images.githubusercontent.com/78699465/114274412-45f5cb80-99ec-11eb-8bdb-2196b3a51dc2.png">

Data Output Sample - The number of retiring employees by title:

<img width="524" alt="Retirement_Titles" src="https://user-images.githubusercontent.com/78699465/114274452-6c1b6b80-99ec-11eb-9b2a-fe081ec74d91.png">

- It was discovered that there were duplicate entries for some employees due to employees having switched titles over the years.
- Using the DISTINCT ON statement, the first occurence of the employee number for each set of rows definds by the ON () clause was retrieved to eliminate the duplicates.
- A new table," Unique Titles" was then created.

DISTINCT ON Statement:

<img width="320" alt="Dinstinct_ON" src="https://user-images.githubusercontent.com/78699465/114274723-d254be00-99ed-11eb-8b82-797cda873519.png">


Data Output Sample - Unique Titles Table:

<img width="422" alt="Unique_Titles_Table" src="https://user-images.githubusercontent.com/78699465/114274730-d97bcc00-99ed-11eb-88ae-25d04c8351f4.png">


- To hold the required information, a new table named. "Retiring Titles" was created by retrieving the number of titles from the Unique Titles table using the COUNT function.

COUNT() Function:

![image](https://user-images.githubusercontent.com/78699465/114275040-01b7fa80-99ef-11eb-9b32-65a0766ed76f.png)

Data Output Sample - Retiring Titles Table:
 
<img width="272" alt="retiring_titles table" src="https://user-images.githubusercontent.com/78699465/114275737-a63b3c00-99f1-11eb-818a-c83c80c876bd.png">





**Employees who are eligible for the Mentorship Program**

- To find the employees eligible for the Mentorship Progem, a new query was written in order to create a table named, "Mentorship Eligiblity".

Query:

<img width="354" alt="Mentorship_Eligible" src="https://user-images.githubusercontent.com/78699465/114275349-3ed0bc80-99f0-11eb-8aa3-b28ef493e8ee.png">

Sample of the result:

<img width="579" alt="Mentorship_Eligibility_table" src="https://user-images.githubusercontent.com/78699465/114275457-7dff0d80-99f0-11eb-9f7f-dae5fcf3f3bb.png">


### Summary

The data shows that there are 90,398 Pewlett Hackard employees reaching or, of retirement age. This appears to be a large number of roles to be filled. A query to find out the total number of employees at Pewlett Hackard would provide better insight. It would also be benificial for providing more detailed data for the Mentorship Program to find out how many mentors are available and how many mentors for a specific job title. This could help the Mentorship Program be more successful if mentees and mentors are matched according to their desired career path and job title.
