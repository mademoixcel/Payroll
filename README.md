# Payroll
 Payroll for 87 employees of company XYZ (Everything in this project was done with Microsoft Excel and Figma)

 # Overview

This Excel payroll project is a comprehensive spreadsheet solution for managing the payroll information and calculations of company XYZ with 87 employees. It includes all relevant formulas and calculations necessary to manage employee data, including hours worked, taxes calculated, gross pay, and net pay.

# Business scenario 
It was on a Friday Afternoon when I logged in to LinkedIn to check my notifications and messages then I got this message from a startup founder.




![linkedin_Chat](https://github.com/mademoixcel/Payroll/assets/124081194/10830fb4-194d-4ef5-b52b-ef2c46cdf686)



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

   
 **Note that I used a [random generator](http://random-name-generator.info/) to generate the names used in this project and a [list randomizer](https://www.randomlists.com/list-randomizer?dup=true&qty=7&items=Founders%2FEntrepreneurs%0AProduct+Development%0AEngineering%2FTechnology%0ASales+and+Business+Development%0AMarketing%0AOperations%0AHuman+Resources%0AFinance+and+Accounting%0ACustomer+Support%0ALegal+and+Compliance) to randomize the departments 87 times to allow for duplicates.**

# Numbering my rows and using RAND() & RANDBETWEEN() 
I used sequence to number my rows, then copied the randomly generated names to my spreadsheet. The males and females names were stacked on top of each other. To get my way around this, I used RAND(). 1st problem solved. Next thing was to give working hours to each employee. I used RANDBETWEEN() to do this, setting my minimum and maximum working hours. I did this for each week in the month of March. I also used RANDBETWEEN() to randomize the amount to be paid to each employee, equally setting the minimum and maximum.


# Features
- Conditional formatting to highlight average earnings of top earners and least earners

- Tracks employee hours worked

- Calculates taxes

- Calculates total net pay

- Uses functions and formulas such as VLOOKUP, COUNTIF, SUMIF, IF, MAXIMUM, MINIMUM, SUM, AVERAGE, shortcuts such as ALT+A+S+S, ALT+H+O+I, ALT+H+O+A, ALT+=, CTRL+SHIFT++

- Drop down list to choose employee id (this will show each employee details)

# Instructions

1 Download the Excel file from GitHub.

2 Open the file and click go to the drop down list.

3 Select employeed id to view employee details.

4 Use the provided formulas to calculate taxes and net pay.

# Contributing

If you would like to contribute to this project, please create an issue or pull request on GitHub.  Known Issues/Bugs: None at this time.  Contact Information: Please submit any questions or feedback related to this project to zehidathabit@gmail.com
