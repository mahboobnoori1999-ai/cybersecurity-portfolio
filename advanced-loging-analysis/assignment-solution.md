# SQL Login Investigation Lab — Assignment & Solutions

## Objective

The purpose of this lab was to investigate login attempt activity using SQL filtering techniques within a MariaDB database environment.

This exercise focused on retrieving authentication data using:
- Date filters
- Time filters
- Numeric filtering
- Range-based filtering

---

# Scenario

As a Security Analyst, I was tasked with analyzing authentication logs stored in the `log_in_attempts` table.

The investigation required retrieving:
- Recent login attempts
- Login activity within a date range
- Authentication events occurring at a specific time
- Information related to a unique login ID

These tasks simulate real-world SOC investigation workflows.

---

# Task 1 — Filter Login Attempts After a Certain Date

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_date > '2023-01-15';
```

## Purpose

Retrieve login attempts occurring after January 15th, 2023.

## Security Relevance

Supports:
- Recent activity investigations
- Threat monitoring
- Authentication analysis

---

# Task 2 — Filter Login Attempts Within a Date Range

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_date BETWEEN '2023-02-01' AND '2023-02-07';
```

## Purpose

Analyze login activity occurring during the first week of February 2023.

## Security Relevance

Supports:
- Timeline investigations
- Incident response
- Threat hunting

---

# Task 3 — Filter Login Attempts at a Specific Time

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_time = '09:30:00';
```

## Purpose

Retrieve all login attempts occurring at exactly 09:30:00.

## Security Relevance

Supports:
- Time-specific event analysis
- Authentication investigations
- Suspicious activity review

---

# Task 4 — Filter Login Attempts by Login ID

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_id = 503;
```

## Purpose

Retrieve information for a specific login attempt.

## Security Relevance

Supports:
- Authentication tracing
- Event auditing
- Security investigations

---

# SQL Concepts Demonstrated

- WHERE clause
- Comparison operators
- BETWEEN operator
- Date filtering
- Time filtering
- Numeric filtering

---

# Conclusion

This lab provided practical experience using SQL to investigate authentication logs and retrieve targeted security information.

By applying comparison operators and range filtering, I strengthened my understanding of:
- Security log analysis
- Database investigations
- Authentication event monitoring
- SOC investigation workflows

These SQL techniques are commonly used by cybersecurity analysts during incident response and threat investigations.

---

# Author

Mahboob Noori  
Aspiring Cybersecurity Analyst
