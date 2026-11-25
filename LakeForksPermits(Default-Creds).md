# Lake Forks Permits -  Penetration Test Report 

## Executive Summary

During the security assessment of the Lake Forks County Permits & Licensing Portal, the staff login credentials were discovered and the internal staff portal was accessed. The default credentials (`admin:admin`) set during the 2018 Wescroft Civic Consulting redesign were left unchanged."

On **93e0ec44-4056-front-counter-4fef2.challenges.webverselabs-pro.com** through **/staff/records** contained the requested flag in the permit-issuance signing key section.

**Key findings:**
- Default staff credentials were active and functional
- Internal staff portal accessible with unauthorized access
- Flag obtained: `WEBVERSE{8e5f8a682....8df}`

## PoC

1. Visit **/login** endpoint
2. Use the credentials `admin:admin`

Observe that you will be logged as an admin user.

<img width="1901" height="1060" alt="image" src="https://github.com/user-attachments/assets/8c39f096-2e45-43fd-8bfb-1b5d2fff53b7" />

Additionally, we have found a statement at the footer giving us hints about the default credentials.

<img width="1862" height="1087" alt="image" src="https://github.com/user-attachments/assets/ba0ef1b2-66d1-4d8d-8746-65e345ca6031" />

## Recommendations

Immediate remediation required:
1. Change default staff credentials immediately
2. Implement mandatory password rotation policy
3. Enable multi-factor authentication for staff accounts
4. Conduct security audit of all default credential configurations
5. Implement password complexity requirements and account lockout policies
6. Review and update the staff login hint text to remove references to default credentials
