# Broken Access Control – OWASP Juice Shop

## Overview
This project demonstrates Broken Access Control vulnerabilities discovered during a VAPT assessment on OWASP Juice Shop.

## Tools Used
- Burp Suite
- Browser Developer Tools
- Kali Linux

## Vulnerability Type
Broken Access Control / Unauthorized Admin Access

## Description
Broken Access Control occurs when applications fail to properly restrict users from accessing privileged functionality.

Admin routes were discoverable through client-side JavaScript analysis and directly accessible without proper authorization validation.

## Steps to Reproduce

1. Open browser developer tools.
2. Inspect the `main.js` file.
3. Search for admin-related routes.
4. Navigate directly to:

```text
http://127.0.0.1:42000/#/administration
```

5. Administrative functionality becomes accessible.

## Impact
- Unauthorized administrative access
- User management compromise
- Full application compromise
- Sensitive information exposure

## Remediation
- Enforce Role-Based Access Control (RBAC)
- Validate permissions server-side
- Restrict access to admin endpoints
- Avoid exposing sensitive routes in client-side code

## Learning Outcome
This project improved understanding of:
- Access control testing
- Client-side route discovery
- Authorization validation
- Administrative endpoint security

## Disclaimer
This assessment was conducted in a legal lab environment using OWASP Juice Shop for educational purposes.
