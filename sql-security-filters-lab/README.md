# SQL Security Filters Lab

## Project Overview

This cybersecurity-focused SQL lab demonstrates how database queries can be used to retrieve and filter organizational security information efficiently.

Using MariaDB and SQL filtering techniques, this project simulates real-world Security Operations Center (SOC) tasks such as:

- Asset identification
- Operating system filtering
- Employee investigation
- Endpoint tracking
- Department-based information retrieval

The lab highlights how security analysts use SQL to support vulnerability management, incident response, and organizational investigations.

---

# Technologies Used

- SQL
- MariaDB
- Linux Terminal
- MySQL-Compatible Database Systems

---

# Cybersecurity Skills Demonstrated

- SQL Query Development
- Database Filtering
- Asset Management
- Security Investigation
- Endpoint Identification
- Organizational Data Analysis
- Pattern Matching with LIKE
- Cybersecurity Documentation

---

# Scenario

As a Security Analyst, I was tasked with retrieving organizational information from a MariaDB database.

The security team required:
- A list of all organization machines
- Systems running a vulnerable operating system
- Employees in specific departments
- Identification of employees using affected machines

SQL filters were applied to retrieve relevant security information quickly and efficiently.

---

# Tasks Completed

## Task 1 — List All Organization Machines

Retrieved all machine IDs and operating systems from the machines table.

### SQL Query

```sql
SELECT device_id, operating_system
FROM machines;
```

### Result

- 200 rows returned
- Displayed all organizational devices and operating systems

### Security Relevance

This query supports:
- Asset inventory management
- Endpoint visibility
- Operating system auditing

---

## Task 2 — Retrieve Machines Running OS 2

Filtered machines running the OS 2 operating system.

### SQL Query

```sql
SELECT device_id, operating_system
FROM machines
WHERE operating_system = 'OS 2';
```

### Result

- 80 machines identified

### Security Relevance

This helps security teams:
- Deploy updates
- Track vulnerable systems
- Perform patch management

---

## Task 3 — Identify Employees in Specific Departments

### Finance Department Query

```sql
SELECT *
FROM employees
WHERE department = 'Finance';
```

### Result

- First employee_id returned: 1003

---

### Sales Department Query

```sql
SELECT *
FROM employees
WHERE department = 'Sales';
```

### Result

- 33 employees returned

### Security Relevance

Supports:
- Security notifications
- Department-specific compliance alerts
- Confidential information handling

---

## Task 4 — Investigate Employee Machines

### Identify Employee in South-109

```sql
SELECT *
FROM employees
WHERE office = 'South-109';
```

### Result

- Employee identified: jlansky

---

### Identify All Employees in South Building

```sql
SELECT *
FROM employees
WHERE office LIKE 'South%';
```

### Result

- First employee belonged to Finance department

### Security Relevance

Supports:
- Incident response
- Building-wide investigations
- Device compromise analysis
- User notification procedures

---

# SQL Concepts Used

- SELECT
- FROM
- WHERE
- LIKE
- Wildcards (%)

---

# Learning Outcomes

Through this lab, I gained practical experience in:
- Writing SQL queries
- Applying SQL filters
- Retrieving security-relevant data
- Investigating organizational assets
- Supporting cybersecurity workflows using databases

---

# Future Improvements

- Add JOIN operations
- Create advanced filtering examples
- Integrate SIEM-style queries
- Simulate real-world incident investigations

---

# Author

Mahboob Noori

Aspiring Cybersecurity Analyst

Focus Areas:
- SOC Operations
- Threat Detection
- SQL Investigations
- Linux Security
- SIEM & Log Analysis
