# Basic-SQL-Filtering

## Project description
Part of my job is to ensure the security of certain database in our organization. I am tasked on monitoring uncommon or suspicious activities and keeping in check if the overall system is safe. For this task, I am assigned on retrieving specifi c data, as well as trace if there are strange activities occurring inside the “employees” and “log_in_att empts” table. The following documentation shows diff erent SQL queries and fi ltering I have implemented to retrieve needed data.

## Retrieve after hours failed login att empts
The company’s working hour ends at “18: 00” and there is a potential for security breach attempts aft er these hours, hence constant monitoring is required. The following code below shows how I created a SQL fi lter to only return the data of failed login att empts aft er the company’s working hour.

![image](https://github.com/user-attachments/assets/ebe66f75-daac-4630-83e4-179160f87458)

I have checked specifically the failed login attempts aft er this hour by using the operator “WHERE” and “>” to fi lter the login att empts made aft er “18: 00” and at the same time, I have utilized operators “AND” to join two conditions: “after 18: 00” and “fail”, as well as “=’ to designate a value which is “0”. “0” denotes to “fail” which is appropriate for the condition and not the counterpart value “1” that denotes “success”.

## Retrieve login attempts on specific dates
A security maintenance was conducted on “2022-05-09” implying a potential for security breach attempts. Normally, the day and the day before of similar activities must be monitored. The following code below shows how I created a SQL filter to only return the data of multiple login attempts made on the specific dates.

![image](https://github.com/user-attachments/assets/eb5463a3-f998-4b9a-853e-f9745d46a3e8)

Hence, I have investigated the “log_in_att empts” table on that specifi c date and the day before it which is “2022-05-08” as these dates are the most vulnerable to threats. Using operators “WHERE” and “Or” to satisfy a condition, the query will retrieve data that are logged either on or before the security maintenance day “2022-05-09” and “2022-05-08”.

## Retrieve login att empts outside of Mexico
Multiple team members reported unusual login activities occurring outside Mexico. The fact that is occurring across diff erent databases’ tables urges immediate action. The following code below shows how I created a SQL fi lter to only return the data of employees with login att empts outside of Mexico.

![image](https://github.com/user-attachments/assets/3b5880b1-b827-4fe9-9650-86dc3bcd7995)

I then proceeded to scan my designated table using the operatorS “WHERE” and “NOT” to filter responses of countries aside “MEXICO”. I have also used operator “LIKE” together with “MEX%” to fi lter out character patt erns starting with “MEX..”, which in the table are commonly “MEXICO”. Using both operator “LIKE” and sign “%” fi ltes patt erns with unspecifi ed characters. The SQL query will now only return the login att empts of individuals that are done
outside of Mexico.

## Retrieve employees in Marketing
This time, I att empted to retrieve employees’ data from the “East” offi ce located in the “Marketing” department for a regular update. I have confi rmed that a single employee’s
machine id needs to be updated.
The following code below shows how I created a SQL fi lter to only return the data of employees assigned on the East section at the Marketing department.

![image](https://github.com/user-attachments/assets/4e403874-ae39-417d-aeb9-5ef2d2466617)

For this query, I deployed operators “WHERE” and “=” to specify the Marketing department. This will consider all employees assigned in the Marketing department. I have also used “AND” operator to join another query condition which is to fi nd offi ces located in the East section. By using operator “LIKE” and sign “%”, unspecifi ed names of offi ces located in the East section will be returned. At this point, the SQL query will only return the data of all employees at East section in the Marketing department.

## Retrieve employees in Finance or Sales
This time I need to retrieve the data of employees that are either present on Finance or Sales department with their designated offi ce and machine information.
The following code below shows how I created a SQL fi lter to only return the data of employees assigned on either specifi ed departments.

![image](https://github.com/user-attachments/assets/7c16fc0d-ea67-4d63-a1e4-10d720cd299a)

Starting by retrieving the data from the employees table, I then input the next line of code for the conditions. I used “WHERE” and “=” operators to specify the department and “OR” to return the data of employees present in either department. I used “OR” because I need the data of all employees that are present in either departments. The “Finance” value in the first condition will return the data of employees present in the Finance department and the “Sales” value in the second condition will return the data of employees present in te Sales department.

## Retrieve all employees not in IT
My last task is to retrieve the data of all employees not in the Information Technology department befor performing an update to their systems. The order of tasks is crucial to thoroughly review and implement a systematic procedure when conducting updates.
The following code below shows how I created a SQL fi lter to return the data of all employees not included in the said department.

![image](https://github.com/user-attachments/assets/a786466e-0f75-4efd-85a4-0ac002d020c9)

To start with, I retrieved the data from the employees table by executing the “FROM” operator. This time, since I only want to retrieve the data of all employees outside the “Information Technology” department, I will be using “WHERE” and “NOT” operator. This will return me the data of employees outside this department.

## Summary
When retrieving the required data, I utilized SQL fi lters to accurately extract them. I operated on tables “employees” and “log_in_att empts” because the data I needed are in these tables. I used operators “AND”, “OR”, and “NOT” to retrieve specifi c information. Lastly, I used operator “LIKE” together with the sign “%” to retrieve data with unspecifi c values or those carrying a specifi c patt e


