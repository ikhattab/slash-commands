---
id: security-audit
name: Security Audit
slug: security
category: code-quality
description: Check code for security vulnerabilities.
---
# Security Audit

Perform a security audit on the selected code. Check for:

1. Injection Attacks: SQL, XSS, command injection
2. Authentication Issues: Weak auth, session problems
3. Data Exposure: PII leaks, sensitive data in logs
4. Access Control: Missing authorization checks
5. Cryptography: Weak algorithms, hardcoded secrets
6. Dependencies: Known vulnerable packages

For each finding:
- Severity: 🔴 Critical / 🟠 High / 🟡 Medium / 🟢 Low
- Description of the vulnerability
- Potential impact
- Recommended fix with code example

Focus on practical, exploitable issues over theoretical concerns.

