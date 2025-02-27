Apply filters to SQL queries

Project Description:

My organization is working to make their system more secure. It is my job to ensure the system is safe, investigate all potential security issues, and update employee computers as needed. The following steps provide examples of how I used SQL with filters to perform security-related tasks.

Retrieve After Hours Failed Login Attempts:

There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated. The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours.

IMAGE

The first part of the screenshot is the query that I created, while the second part is the output from the query. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the log_in_attempts table. Following this, I used a WHERE clause with an AND operator to filter my results to only include login attempts that occurred after 18:00 and were unsuccessful. The first condition is login_time > ’18:00’, which filters for login attempts that occurred after 18:00. The second condition is success = FALSE, which filters for failed login attempts.

Retrieve Login Attempts on Specific Dates:

A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated. The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.

IMAGE

The first part of the screenshot is the query that I created, while the second part is the output from the query. This query filters for all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I started by selecting all data from the log_in_attempts table. Following this, I used a WHERE clause with an OR operator to filter my results to only show login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is login_date = ‘2022-05-09’, which filters for login attempts that occurred on 2022-05-09. The second condition is login_date = ‘2022-05-08’, which filters for login attempts that occurred on 2022-05-08.

Retrieve Login Attempts Outside of Mexico:

After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated. The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico.

IMAGE

The first part of the screenshot is the query that I created, while the second part is the output from the query. This query filters for all login attempts that originated from any country other than Mexico. First, I started by selecting all data from the log_in_attempts table. Following this, I used a WHERE clause with the NOT operator to filter for countries other than Mexico. I used LIKE with MEX% as the pattern to match since the dataset represents Mexico as MEX and MEXICO. The percentage sign (%) represents any number of unspecified characters when used with LIKE. This condition appears as WHERE NOT country LIKE ‘MEX%’ in the query.

Retrieve Employees in Marketing:

My team wants to update the computers for certain employees in the Marketing department. To do this, I have to get information on which employee machines to update. The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building.

IMAGE

The first part of the screenshot is the query that I created, while the second part is the output from the query. This query filters for all employees in the Marketing department that are located in the East building. First, I started by selecting all data from the employees table. Following this, I used a WHERE clause with the AND operator to filter for employees who work in the Marketing department in the East building. I used LIKE with East% as the pattern to match because the data in the office column represents the East building along with the specific office number. The first condition is the department = ‘Marketing’ portion, which filters for employees in the Marketing department. The second condition is the office LIKE ‘East%’ portion, which filters for employees in the East building.

Retrieve Employees in Finance or Sales:

The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is needed, I have to get information on employees only from these two departments. The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Finance or Sales departments.

IMAGE

The first part of the screenshot is the query that I created, while the second part is the output from the query. This query filters for all employees in the Finance and Sales departments. First, I started by selecting all data from the employees table. Following this, I used a WHERE clause with the OR operator to filter for employees who are in the Finance and Sales departments. I used the OR operator instead of AND since I want to return all employees who are in either department, rather employees who are in both. The first condition is department = ‘Finance’, which filters for employees in the Finance department. The second condition is department = ‘Sales’ which filters for employees in the Sales department.

Retrieve All Employees Not in IT:

My team needs to make one more security update on employees who are not in the Information Technology department. To make the update, I first have to get information on these employees. The following demonstrates how I created a SQL query to filter for employee machines from employees not in the Information Technology department.

IMAGE

The first part of the screenshot is the query that I created, while the second part is the output from the query. This query filters for all employees that are not in the Information Technology department. First, I started by selecting all data from the employees table. Following this, I used a WHERE clause with the NOT operator to filter for employees that do not belong to the Information Technology department. This condition appears as WHERE NOT department = ‘Information Technology’ in the query.

Summary:

I applied filters to SQL queries to pull specific information on login attempts and employee machines. I used two different tables titled log_in_attempts and employees. I used the AND, OR, and NOT operators to filter for the specific information needed for each task. I also used LIKE and the percentage sign (%) wildcard to filter for patterns.


