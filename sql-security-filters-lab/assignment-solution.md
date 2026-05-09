# SQL Security Filters Lab — Assignment & Solutions

## Objective

The purpose of this lab was to apply SQL filtering techniques in a MariaDB environment to retrieve security-related organizational information efficiently.

---

# Scenario

As a Security Analyst, I was responsible for querying organizational databases to retrieve information related to:
- Machines and operating systems
- Employees and departments
- Office locations
- Security investigations

The retrieved information supports:
- Vulnerability management
- Security notifications
- Endpoint investigations
- Incident response activities

---

# Task 1 — List All Organization Machines

## Problem

Retrieve all organization machines and their operating systems from the machines table.

---

## SQL Query

```sql
SELECT device_id, operating_system
FROM machines;
```

---

## Result

- Returned 200 rows
- Displayed all device IDs and operating systems

---

## Security Purpose

This query supports:
- Asset inventory management
- Device visibility
- Operating system tracking

---

# Task 2 — Retrieve Machines Running OS 2

## Problem

Identify all machines using the OS 2 operating system.

---

## SQL Query

```sql
SELECT device_id, operating_system
FROM machines
WHERE operating_system = 'OS 2';
```

---

## Result

- Returned 80 rows
- Identified all systems using OS 2

---

## Security Purpose

Useful for:
- Patch deployment
- Vulnerability management
- Security updates

---

# Task 3 — Identify Employees in Specific Departments

## Problem 1

Retrieve all employees working in the Finance department.

---

## SQL Query

```sql
SELECT *
FROM employees
WHERE department = 'Finance';
```

---

## Result

- First employee_id returned: 1003

---

## Problem 2

Retrieve all employees working in the Sales department.

---

## SQL Query

```sql
SELECT *
FROM employees
WHERE department = 'Sales';
```

---

## Result

- 33 employees returned

---

## Security Purpose

These queries support:
- Confidentiality notices
- Department-specific alerts
- Compliance operations

---

# Task 4 — Investigate Employee Machines

## Problem 1

Identify the employee assigned to office South-109.

---

## SQL Query

```sql
SELECT *
FROM employees
WHERE office = 'South-109';
```

---

## Result

- Employee identified: jlansky

---

## Problem 2

Retrieve all employees located in the South building.

---

## SQL Query

```sql
SELECT *
FROM employees
WHERE office LIKE 'South%';
```

---

## Result

- First employee belonged to Finance department

---

## Security Purpose

Supports:
- Incident response investigations
- Building-wide device investigations
- Security alert distribution

---

# SQL Concepts Demonstrated

- SELECT statements
- WHERE clause filtering
- Pattern matching using LIKE
- Wildcard filtering with %

---

# Conclusion

This lab provided hands-on experience using SQL within a cybersecurity context. By applying filters and pattern matching techniques, I was able to retrieve security-related organizational information efficiently and support simulated SOC investigation workflows.

The project strengthened my understanding of:
- Database investigations
- SQL filtering
- Organizational asset tracking
- Security-focused data analysis

---

# Author

Mahboob Noori  
Aspiring Cybersecurity Analyst
