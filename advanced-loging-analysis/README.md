# SQL Login Investigation Lab

## Project Overview

This cybersecurity-focused SQL lab demonstrates how database filtering techniques can be used to investigate login activity and authentication events within an enterprise environment.

Using MariaDB and SQL comparison operators, the project simulates real-world Security Operations Center (SOC) investigations involving:
- Login attempt analysis
- Date-based filtering
- Time-specific event analysis
- Authentication tracking
- Login ID investigations

The lab highlights how security analysts use SQL to analyze security logs and identify suspicious or targeted authentication activity.

---

# Technologies Used

- SQL
- MariaDB
- Linux Terminal
- MySQL-Compatible Database Systems

---

# Cybersecurity Skills Demonstrated

- SQL Query Development
- Authentication Log Analysis
- Security Event Investigation
- Date and Time Filtering
- Database Investigation
- Security Monitoring
- SOC Investigation Workflow
- Security Documentation

---

# Scenario

As a Security Analyst, I was tasked with investigating login attempt activity stored in the `log_in_attempts` database table.

The investigation required:
- Filtering login attempts after a certain date
- Analyzing authentication activity during a specific date range
- Investigating login attempts at a specific time
- Retrieving information using unique login IDs

These activities simulate real-world SOC investigation and threat analysis workflows.

---

# Task 1 — Filter Login Attempts After a Certain Date

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_date > '2023-01-15';
```

## Security Relevance

This query helps analysts:
- Investigate recent authentication activity
- Monitor post-incident login attempts
- Analyze suspicious access patterns

---

# Task 2 — Filter Login Attempts Within a Date Range

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_date BETWEEN '2023-02-01' AND '2023-02-07';
```

## Security Relevance

Supports:
- Timeline investigations
- Incident scoping
- Threat hunting activities

---

# Task 3 — Filter Login Attempts at a Specific Time

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_time = '09:30:00';
```

## Security Relevance

Useful for:
- Time-based incident analysis
- Identifying coordinated login activity
- Investigating suspicious authentication events

---

# Task 4 — Filter Login Attempts by Login ID

## SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_id = 503;
```

## Security Relevance

Supports:
- Individual event investigations
- Authentication trace analysis
- Security auditing

---

# SQL Concepts Used

- WHERE
- >
- =
- BETWEEN
- Date Filtering
- Time Filtering
- Numeric Filtering

---

# Learning Outcomes

Through this lab, I gained practical experience in:
- Security log analysis using SQL
- Filtering authentication events
- Conducting timeline-based investigations
- Querying databases for incident response support
- Investigating targeted login events

---

# Future Improvements

- Add failed login analysis
- Detect brute-force attempts
- Build advanced authentication queries
- Integrate SIEM-style workflows
- Add JOIN operations for user correlation

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
