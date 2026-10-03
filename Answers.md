# Answers to Part 3

Add your answers to the questions in Part 3, Step 2 below. 

## Vulernability Remediation:
### Vulnerability 1: 
1. Which package or library are you addressing?
PyJWT
2. Which CVE is linked to this vulnerability?
CVE-2026-102268. This VUlnerability can allow an attacker to forge valid JWT tokens when an application mixes HMAC and asymmetric signature algorithms. Certain malformed PEM public keys may incorrectly be accepted as HMAC secrets.
3. What remediation steps do you suggest?
Upgrade PyJWT to version 2.14.0 or later, which contains the fix. Applications should also avoid mixing HMAC and asymmetric algorithms in the same JWT verification configuration.
### Vulnerability 2:
1. Which vulnerability are you addressing?
PyYAML
2. Which CVE is linked to this vulnerability?
CVE-2019-20477. This vulnerability involves unsafe deserialization in PyYAML's load and load_all functions, which can allow untrusted YAML data to cause arbitrary code execution
3. What remediation steps do you suggest? 
Upgrade PyYAML to version 5.2 or later, which contains the fix. The application should also avoid loading untrusted YAML with unsafe loaders and use safe_load when possible.