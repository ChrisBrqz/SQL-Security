# SQL-Security log Analysis

This project showcases how SQL can be used to perform investigative analysis on system login attempts and employee machines for cybersecurity and IT operations.

Using a MariaDB database with two tables — `log_in_attempts` and `employees` — I performed security-related tasks including filtering failed logins, isolating logins by country or time, and identifying employees by department or location.


Project Contents
log_in_attempts table:** Contains login event metadata (timestamp, IP, success/failure)
employees table:** Holds user, department, and office location info
- SQL query walkthroughs with:
  - After-hours login filtering
  - Country-based login analysis
  - Departmental and building-based employee queries

Use Case:
This portfolio simulates a SOC analyst’s responsibilities:
- Investigating failed login activity
- Isolating suspicious geolocations
- Retrieving employee device data for patching or upgrades

---

Key Concepts Demonstrated

- SQL `WHERE`, `AND`, `OR`, and `NOT` clauses  
- Pattern matching using `LIKE` and `%`  
- Combining filters to isolate high-risk events  
- Reading table schemas for structured analysis  
- Interpreting and writing structured queries



Example Query
```sql
SELECT * 
FROM log_in_attempts 
WHERE login_time > '18:00' AND success = FALSE;

This SQL project demonstrates how data filtering and analysis can support cybersecurity investigations. By using core SQL logic and real-world security scenarios, this portfolio shows my ability to interpret data logs, isolate risks, and support operational response through structured queries.
