# Google-course---Apply-filters-to-SQL-queries
Project Description
In this project, I used SQL to filter data and investigate potential security issues in the organization's database. By applying logical operators such as AND, OR, and NOT, I was able to retrieve targeted data from the employees and log_in_attempts tables. This process demonstrates my ability to analyze login attempts and employee information while ensuring security protocols are maintained.

Queries and Explanations
1. Retrieve After-Hours Failed Login Attempts
Query:

sql
Copy code
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = 0;
Explanation:

This query retrieves all failed login attempts (success = 0) that occurred after 6:00 PM (login_time > '18:00').
The AND operator ensures both conditions are met.
This is useful for investigating suspicious activity outside of business hours.
2. Retrieve Login Attempts on Specific Dates
Query:

sql
Copy code
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';
Explanation:

The query selects all login attempts that occurred on either May 8 or May 9, 2022.
The OR operator ensures that attempts from both dates are included.
This helps narrow down activity surrounding a specific incident.
3. Retrieve Login Attempts Outside of Mexico
Query:

sql
Copy code
SELECT *
FROM log_in_attempts
WHERE country NOT LIKE '%MEX%';
Explanation:

This query retrieves all login attempts where the country is not MEX or MEXICO.
The NOT LIKE operator excludes rows matching the specified pattern %MEX%.
The % wildcard ensures any text containing "MEX" is matched, regardless of case or additional characters.
4. Retrieve Employees in Marketing in the East Building
Query:

sql
Copy code
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East-%';
Explanation:

This query retrieves all employees in the Marketing department who work in the East building.
The LIKE 'East-%' condition filters for any office name starting with "East-" (e.g., East-170).
The AND operator ensures both conditions are satisfied.
5. Retrieve Employees in Finance or Sales Departments
Query:

sql
Copy code
SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';
Explanation:

This query retrieves employees working in either the Finance or Sales departments.
The OR operator includes rows from both departments.
This query is useful for targeting updates for specific teams.
6. Retrieve All Employees Not in IT
Query:

sql
Copy code
SELECT *
FROM employees
WHERE department != 'Information Technology';
Explanation:

This query retrieves all employees who are not in the Information Technology department.
The != operator excludes rows where department equals "Information Technology."
This ensures updates are applied to all other departments.
Summary
This project demonstrated the use of SQL filters to retrieve targeted data from organizational databases. Queries included filtering for specific dates, times, and patterns using AND, OR, NOT, and LIKE operators. By investigating login attempts and employee information, I highlighted my ability to analyze data and respond to security concerns effectively. These SQL skills are critical for ensuring database integrity and maintaining organizational security.
