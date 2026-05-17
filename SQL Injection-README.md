# SQL Injection Vulnerability Analysis – OWASP Juice Shop

## Overview
This project demonstrates a practical SQL Injection vulnerability identified in the OWASP Juice Shop application during a Vulnerability Assessment and Penetration Testing (VAPT) exercise.

## Tools Used
- Burp Suite
- Kali Linux
- OWASP Juice Shop

## Vulnerability Type
SQL Injection (Authentication Bypass)

## Description
SQL Injection occurs when user-controlled input is improperly sanitized before being used in SQL queries. This allows attackers to manipulate backend database queries.

During testing, the login functionality of OWASP Juice Shop was found vulnerable to SQL Injection, enabling authentication bypass.

## Steps to Reproduce

1. Open the OWASP Juice Shop login page.
2. Intercept the login request using Burp Suite.
3. Modify the login payload with:

```sql
' OR 1=1 --
