# SQL Logical Operators Lab

## Project Overview

This cybersecurity-focused SQL lab demonstrates how logical operators can be used to retrieve targeted security information from organizational databases.

Using MariaDB and SQL filtering techniques, this project simulates real-world Security Operations Center (SOC) investigations involving:
- Failed login analysis
- Date-based authentication investigations
- Country-based filtering
- Department-specific employee analysis
- Endpoint update investigations

The lab highlights how cybersecurity analysts use SQL logical operators such as:
- AND
- OR
- NOT
- LIKE

to investigate security events and organizational assets efficiently.

---

# Technologies Used

- SQL
- MariaDB
- Linux Terminal
- MySQL-Compatible Database Systems

---

# Cybersecurity Skills Demonstrated

- SQL Query Development
- Security Log Analysis
- Authentication Investigation
- Database Filtering
- Endpoint Investigation
- Security Event Monitoring
- Pattern Matching
- Logical Query Operations
- SOC Investigation Workflow

---

# Scenario

As a Security Analyst, I was responsible for retrieving targeted information from the organization database to support:
- Security investigations
- Employee machine updates
- Authentication analysis
- Department-based security operations

The investigation required filtering login attempts and employee records using multiple SQL logical operators and conditions.

---

# Task 1 — Retrieve After-Hours Failed Login Attempts

## Objective

Identify all failed login attempts that occurred after business hours (after 18:00).

---

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00'
AND success = FALSE;
```

---

## Result

- 19 failed login attempts occurred after 18:00

---

## Security Relevance

This query supports:
- Suspicious login investigations
- After-hours access monitoring
- Threat detection
- Authentication auditing

---

# Task 2 — Retrieve Login Attempts on Specific Dates

## Objective

Investigate login attempts that occurred on:
- 2022-05-08
- 2022-05-09

---

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09'
OR login_date = '2022-05-08';
```

---

## Result

- 75 login attempts were identified across the two days

---

## Security Relevance

Supports:
- Timeline analysis
- Incident investigations
- Threat hunting activities
- Authentication event review

---

# Task 3 — Retrieve Login Attempts Outside of Mexico

## Objective

Identify login attempts that did not originate from Mexico.

The country field contained:
- MEX
- MEXICO

The LIKE operator and wildcard filtering were used.

---

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

---

## Result

- 144 login attempts originated outside of Mexico

---

## Security Relevance

Supports:
- Geographic login investigations
- Threat intelligence analysis
- Suspicious access detection
- Foreign login monitoring

---

# Task 4 — Retrieve Marketing Employees in East Building

## Objective

Retrieve employees in the Marketing department located in East building offices.

---

## SQL Query

```sql
SELECT *
FROM employees
WHERE department = 'Marketing'
AND office LIKE 'East%';
```

---

## Result

- First employee username: elarson

---

## Security Relevance

Supports:
- Endpoint update operations
- Department-based investigations
- Building-specific device management

---

# Task 5 — Retrieve Employees in Finance or Sales

## Objective

Retrieve employee records for users in:
- Finance
- Sales

---

## SQL Query

```sql
SELECT *
FROM employees
WHERE department = 'Finance'
OR department = 'Sales';
```

---

## Result

- First employee username in Sales: lrodriqu

---

## Security Relevance

Supports:
- Department-wide update operations
- Confidentiality notifications
- Compliance-related investigations

---

# Task 6 — Retrieve Employees Not in Information Technology

## Objective

Retrieve records for employees who are not in the Information Technology department.

---

## SQL Query

```sql
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```

---

## Result

- 161 employees were not in Information Technology

---

## Security Relevance

Supports:
- Exclusion-based investigations
- Remaining endpoint update operations
- Departmental security management

---

# SQL Concepts Demonstrated

- SELECT
- WHERE
- AND
- OR
- NOT
- LIKE
- Wildcard Matching (%)

---

# Learning Outcomes

Through this lab, I gained practical experience in:
- Applying SQL logical operators
- Filtering authentication logs
- Investigating organizational data
- Conducting department-based analysis
- Supporting cybersecurity workflows using SQL

---

# Future Improvements

- Add JOIN operations
- Correlate employee and device data
- Simulate SIEM investigations
- Build advanced authentication analysis queries
- Detect suspicious login patterns

---

# Conclusion

This lab strengthened my ability to use SQL logical operators to investigate authentication events and retrieve targeted security information from organizational databases.

By applying:
- AND
- OR
- NOT
- LIKE

I improved my understanding of:
- Security log analysis
- Database investigations
- Authentication monitoring
- SOC investigation workflows

These techniques are commonly used by cybersecurity analysts during incident response and threat hunting operations.

---

# Author

Mahboob Noori

Aspiring Cybersecurity Analyst

Focus Areas:
- SOC Operations
- Threat Detection
- SQL Investigation
- Security Log Analysis
- SIEM & Incident Response
