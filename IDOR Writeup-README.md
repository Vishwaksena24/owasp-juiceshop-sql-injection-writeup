# IDOR Vulnerability Analysis – OWASP Juice Shop

## Overview
This project demonstrates the discovery and exploitation of an Insecure Direct Object Reference (IDOR) vulnerability in OWASP Juice Shop.

## Tools Used
- Burp Suite
- Kali Linux
- OWASP Juice Shop

## Vulnerability Type
IDOR (Insecure Direct Object Reference)

## Description
IDOR vulnerabilities occur when applications expose internal object references such as user IDs without proper authorization checks.

During testing, basket details belonging to other users were accessible by modifying request parameters.

## Steps to Reproduce

1. Log in as a normal user.
2. Add items to the basket.
3. Intercept the basket request using Burp Suite.
4. Observe the request:

```http
GET /rest/basket/6 HTTP/1.1
```

5. Modify the basket ID:

```http
GET /rest/basket/2 HTTP/1.1
```

6. Forward the request.
7. Another user’s basket information becomes visible.

## Impact
- Unauthorized access to user data
- Privacy violations
- Sensitive information disclosure
- Possible account manipulation

## Remediation
- Implement proper authorization checks
- Validate object ownership server-side
- Avoid exposing direct object references
- Use session-based authorization validation

## Learning Outcome
This project provided hands-on experience in:
- Access control testing
- Request manipulation
- Authorization bypass validation
- Web application penetration testing

## Disclaimer
Testing was conducted only on OWASP Juice Shop in a controlled educational environment.
