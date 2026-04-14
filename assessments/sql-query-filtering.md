# Apply Filters with SQL Queries – Security Investigation

## Project Description
In this activity, I investigated potential security issues by querying employee and login data using SQL.  
The objective was to identify suspicious login behavior, review affected users, and support security updates by filtering records based on time, date, location, and department.

---

## Retrieve After-Hours Failed Login Attempts

Query: ```
```
    SELECT *
    FROM log_in_attempts
    WHERE login_time > '18:00' AND success = 0;
```

Explanation:  
This query retrieves all failed login attempts that occurred after business hours.  
Filtering by time and failure status helps identify potentially malicious authentication attempts outside normal operating periods.

---

## Retrieve Login Attempts on Specific Dates

Query:```
``` SELECT *
    FROM log_in_attempts
    WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```
Explanation:  
This query retrieves all login attempts from the day a suspicious event was reported and the day before.  
It supports timeline analysis during incident investigation.

---

## Retrieve Login Attempts Outside of Mexico

Query: ```
```
    SELECT *
    FROM log_in_attempts
    WHERE NOT country LIKE 'MEX%';
```
Explanation:  
This query filters out login attempts originating from Mexico.  
The LIKE operator with a wildcard (%) ensures that both “MEX” and “MEXICO” values are excluded.

---

## Retrieve Employees in Marketing (East Building)

Query:```
```
    SELECT *
    FROM employees
    WHERE department = 'Marketing' AND office LIKE 'East%';
```
Explanation:  
This query identifies all Marketing department employees located in the East building.  
It uses AND to combine conditions and LIKE to match office naming patterns.

---

## Retrieve Employees in Finance or Sales

Query: ```
```
    SELECT *
    FROM employees
    WHERE department = 'Finance' OR department = 'Sales';
```
Explanation:  
This query retrieves employees from either the Finance or Sales departments.  
The OR operator allows filtering across multiple departments.

---

## Retrieve Employees Not in IT

Query:```
```
    SELECT *
    FROM employees
    WHERE NOT department = 'Information Technology';
```
Explanation:  
This query identifies all employees outside the IT department.  
It helps scope security updates to systems that have not yet been patched.

---

## Summary
This activity demonstrates the use of SQL filtering in a security context to investigate incidents, detect abnormal behavior, and support remediation efforts.  
It highlights practical use of AND, OR, NOT, LIKE, and date/time filters in real-world security investigations.
