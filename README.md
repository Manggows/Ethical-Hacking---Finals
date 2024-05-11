
# Ethical Hacking Technical Report
#### Client: Lazada
#### Date: May 11, 2024
#### Prepared by: Lyka Mae F. Viñas


# Technical Report: Vulnerability Assessment of Lazada

## Executive Summary:
This report presents the technical findings of the ethical hacking assessment conducted for Lazada. The assessment aimed to identify vulnerabilities within the organization's network infrastructure, applications, and systems. Through various testing methodologies, critical and high-risk issues were discovered. This report provides detailed descriptions of these findings, along with actionable recommendations for remediation.

## Vulnerability Summary:

1. **SQL Injection in User Authentication:**
   - *Critical:* Lazada's user authentication system is vulnerable to SQL injection attacks, potentially allowing attackers to bypass authentication mechanisms and gain unauthorized access to user accounts or sensitive data.

2. **Cross-Site Scripting (XSS) in Product Reviews:**
   - *Critical:* The product review section of Lazada's website is susceptible to XSS attacks, enabling attackers to inject malicious scripts into the page viewed by other users, leading to potential data theft or manipulation.

3. **Insecure Direct Object References (IDOR) in Order Management:**
   - *High:* Lazada's order management system lacks proper access controls, allowing users to access orders and data that they should not have permissions for, leading to potential data exposure and privacy violations.

4. **Weak Password Policies:**
   - *High:* Lazada's password policies are weak, allowing users to create weak passwords that are easily guessable or susceptible to brute force attacks, increasing the risk of unauthorized access to user accounts.

5. **Unvalidated Redirects and Forwards:**
   - *High:* Lazada's website contains unvalidated redirects and forwards, which can be exploited by attackers to redirect users to malicious websites, phishing pages, or other harmful destinations.

6. **Security Misconfigurations in Cloud Infrastructure:**
   - *High:* Lazada's cloud infrastructure is misconfigured, exposing sensitive data and services to potential exploitation by attackers, such as publicly accessible storage buckets or improperly configured security groups.

7. **Sensitive Data Exposure:**
   - *High:* Lazada stores sensitive customer information, such as payment details, without proper encryption, leaving it vulnerable to unauthorized access or interception by attackers.

8. **Outdated Software and Patch Management:**
   - *High:* Lazada's systems and software are not regularly updated with security patches, leaving them vulnerable to known vulnerabilities and exploits.

9. **Insecure APIs:**
   - *High:* Lazada's APIs lack proper authentication and authorization mechanisms, allowing attackers to access sensitive data or perform unauthorized actions by exploiting weaknesses in API security.

10. **Lack of Web Application Firewall (WAF):**
    - *High:* Lazada's web applications lack a WAF, leaving them vulnerable to various web-based attacks, such as SQL injection, XSS, and CSRF, which could lead to data breaches or compromise of user accounts.

## Recommendations:

1. **SQL Injection in User Authentication:**
   - Implement parameterized queries or prepared statements to sanitize user input and prevent SQL injection attacks.
   - Use secure authentication mechanisms such as bcrypt for password hashing to mitigate the risk of credential theft.

2. **Cross-Site Scripting (XSS) in Product Reviews:**
   - Implement input validation and output encoding to sanitize user-generated content and prevent XSS attacks.
   - Regularly scan and audit web applications for security vulnerabilities, including XSS, using automated tools and manual testing.

3. **Insecure Direct Object References (IDOR) in Order Management:**
   - Implement proper access controls and authorization mechanisms to restrict user access to authorized resources only.
   - Ensure that sensitive data is properly protected and accessed only by authenticated and authorized users.

4. **Weak Password Policies:**
   - Enforce strong password policies, including minimum length requirements, complexity rules, and regular password expiration.
   - Implement multi-factor authentication (MFA) to add an extra layer of security to user accounts.

5. **Unvalidated Redirects and Forwards:**
   - Validate and sanitize all user-supplied input to prevent redirection to untrusted or malicious URLs.
   - Use a whitelist approach to validate redirect URLs and ensure that they only point to trusted domains.

6. **Security Misconfigurations in Cloud Infrastructure:**
   - Conduct regular security assessments and audits of cloud infrastructure configurations to identify and remediate security misconfigurations.
   - Implement security automation tools and scripts to enforce security best practices and configurations.

7. **Sensitive Data Exposure:**
   - Encrypt sensitive data at rest and in transit using strong encryption algorithms and protocols.
   - Implement access controls and data classification policies to restrict access to sensitive data to authorized users only.

8. **Outdated Software and Patch Management:**
   - Establish a robust patch management process to ensure timely installation of security patches and updates for all systems and software components.
   - Implement vulnerability scanning and management tools to identify and prioritize patching of critical vulnerabilities.

9. **Insecure APIs:**
   - Implement proper authentication and authorization mechanisms such as OAuth or JWT tokens to secure APIs.
   - Conduct regular security assessments and penetration testing of APIs to identify and remediate security vulnerabilities.

10. **Lack of Web Application Firewall (WAF):**
    - Deploy a WAF to monitor and filter HTTP traffic to web applications, blocking common web-based attacks such as SQL injection, XSS, and CSRF.
    - Regularly update and tune WAF rules to adapt to emerging threats and protect against new attack vectors.

## Conclusion:
The vulnerabilities identified in this assessment pose significant risks to the security and integrity of Lazada's infrastructure and data. By implementing the recommended remediation measures, Lazada can enhance its security posture and better protect against potential cyber threats and data breaches.
