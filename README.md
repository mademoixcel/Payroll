 Everything in this project was done with Microsoft Excel and Figma.

 # Overview

This Excel payroll project is a comprehensive spreadsheet solution for managing the payroll information and calculations of company XYZ with 87 employees. It includes all relevant formulas and calculations necessary to manage employee data, including hours worked, taxes calculated, gross pay, and net pay.

# Instructions

1 Download the Excel file from GitHub.

2 Open the file and click go to the drop-down list.

3 Select employee id to view employee details.

4 Use the provided formulas to calculate taxes and net pay.


# Features
- Conditional formatting to highlight top earners and least earners

- Tracks employee hours worked

- Calculates taxes

- Calculates total net pay

- Uses functions and formulas such as VLOOKUP, COUNTIF, IF, MAXIMUM, MINIMUM, SUM, AVERAGE, shortcuts such as ALT+A+S+S, ALT+H+O+I, ALT+H+O+A, ALT+=, CTRL+SHIFT++

- Drop down list to choose employee id 

# Business scenario 
It was on a Friday Afternoon when I logged in to LinkedIn to check my notifications and messages then I got this message from a startup founder.




![linkedin_Chat (1)](https://github.com/mademoixcel/Payroll/assets/124081194/7eb8c99d-7e83-444b-915a-74208c8854bd)




**Please note that this message is entirely fictional and should not be used for any deceptive purposes.**



Apparently, the company expanded in a short period of time and they haven't been able to keep track of their employee's payments for a month. So, guess who would be doing that? ME. 
Fast forward to Monday, we had a brief call to discuss in detail what the company wanted. I got the file after the call. It was in xlsx format. The data contained:

# Details of Dataset
1. Employee id
2. first name
3. last name
4. Gender
5. Department 
6. Amount earned (per hour)
7. Weekly hours worked

   
 **Note that I used a [random generator](http://random-name-generator.info/) to generate the names used in this project and a [list randomizer](https://www.randomlists.com/list-randomizer?dup=true&qty=7&items=Founders%2FEntrepreneurs%0AProduct+Development%0AEngineering%2FTechnology%0ASales+and+Business+Development%0AMarketing%0AOperations%0AHuman+Resources%0AFinance+and+Accounting%0ACustomer+Support%0ALegal+and+Compliance) to randomize the departments to allow for duplicates.**

# Numbering my rows and using RAND() & RANDBETWEEN() 
I used SEQUENCE() to number my rows, then copied the randomly generated names to my spreadsheet. The male's and female's names were stacked on top of each other. To get my way around this, I used RAND(). 1st problem was solved. The next thing was to give working hours to each employee. I used RANDBETWEEN() to do this, setting the minimum and maximum working hours. I did this for each week in the month of March. I also used RANDBETWEEN() to randomize the amount to be paid to each employee, equally setting the minimum and maximum.

![Screenshot (997)](https://github.com/mademoixcel/Payroll/assets/124081194/fb8c6070-c07d-4e5c-b778-142c0c912c40)


# Calculating Pay for each week using SUM()

I calculated the salary for each employee by multiplying the amount paid per hour and hours_worked. This was done using =hourly_wage*number_of_hours_worked, then filling down for the rest of the rows.

# Overtime and  Overtime Payment

The client asked to calculate the overtime pay for each employee by giving each employee 1/4 of their hourly wage only if they work overtime, stating that any employee that's working between 31 to 40 hours per week is using overtime. To do this, I first calculated the overtime hours using =IF(column['hours_worked']>30, column['hours_worked']-30,0). This will subtract the working hour from 30, only if the working hour is greater than 30, else it should be zero. After that, I calculated the overtime payment using (0.25*'salary paid per hour'*overtime_hours)

# Gross pay for each week
I calculated the gross pay for each week by adding the overtime payment and the salary, then named and gave color to each week to be able to differentiate them.

![Screenshot (999)](https://github.com/mademoixcel/Payroll/assets/124081194/6ad92200-d51f-4127-8350-9767790c8199)

# Total Gross pay, Tax, and Net pay
I calculated the gross pay by adding the total gross pay for each week, then removed the 7% tax. I did this by using =(0.007 * gross pay). This calculated the gross pay for each employee, then I calculated the net pay by subtracting the tax from gross pay.

![Screenshot (1010)](https://github.com/mademoixcel/Payroll/assets/124081194/1d20d522-304d-4446-9e1a-7b4a333d0c30)


# How many people are in the organization

I used COUNTIF() for this using 'Male' and 'Female' respectively for the criteria of each COUNTIF(). The result showed there are 52 Males and 35 Females. Overall, there are 87 people in the organization.


<img width="1705" alt="Untitled (27)" src="https://github.com/mademoixcel/Payroll/assets/124081194/f363cd09-690a-433b-8fd4-67995406d19e">


# How many people are in each department?
To do this, I used a pivot table to get the statistics of the number of people in each department, then used Figma to visualize it
<img width="2402" alt="voice activated app Diagram (Community) (8)" src="https://github.com/mademoixcel/Payroll/assets/124081194/76e38a8b-8b88-40e0-b7c4-d21369cee00e">
The marketing department has the highest number of employees while sales and business development has the least.


# Getting the top net pay and using conditional formatting to highlight 
Top net pay can easily be gotten by selecting all rows and columns using CTRL A and ALT+A+S+D to sort the values in descending order. The next thing I did was to use conditional formatting to highlight the values that appeared in the top 10. These values are the top 10 net pay for the month of March.

![Screenshot (1012)](https://github.com/mademoixcel/Payroll/assets/124081194/a3b8c975-5d4d-4c8a-af5e-1eca55ce6933)

# Who are the top 3 earners?
![WhatsApp Image 2023-07-12 at 12 46 05 PM (1)](https://github.com/mademoixcel/Payroll/assets/124081194/fe90809b-cd5a-4e7f-bc21-595a2bd847b5)
The top 3 earners are:
1. **Bobby Robinson** from the department of Sales and Business Development with a monthly net pay of $3,510.00
2. **Christina Jackson** from the department of  Sales and Business Development with a monthly net pay of $3,369.90
3. **Donna Diaz** from the department of Product Development with a monthly net pay of $3,287.70

Click here to read all the steps taken to create this project
