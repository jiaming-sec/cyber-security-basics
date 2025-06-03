## Common Security Concepts

---

## CIA Triads
- Confidentiality: Keep data private (e.g., encryption).
- Integrity: Ensure data isn't tampered with (e.g., checksums).
- Availability: Make sure systems are up and accessible (e.g., redundant systems).
## AuthN and AuthZ
**AuthN (Authentication)**
- Proves who you are (e.g., login with username + password).
  
**AuthZ (Authorization)**
- Defines what you're allowed to do (e.g., read-only access vs admin).
## MFA (Multi-Factor Authentication)
- Using two or more of: something you know (password), have (phone), or are (fingerprint).
## 2FA (Two-Factor Authentication)
- A type of MFA using exactly two different factors.
## OAuth2.0
- A secure authorization protocol: lets apps access your data without sharing your password (e.g., "Login with Google").
## SSO (Single Sign-On)
- Login once, access many systems (e.g., Google account to access Gmail, Drive, YouTube).
## OIDC and SAML
**(OpenID Connect)**
- Built on OAuth 2.0, adds authentication (identity info) for logging in.

**SAML (Security Assertion Markup Language)**
- XML-based standard for SSO used in enterprise apps.
## Malware
- Malicious software (broad category): viruses, ransomware, spyware, etc.
## Virus
- Malicious code that spreads when you open infected files/programs.
## Ransomware
- Malware that encrypts your files and demands payment to unlock them.
## Spam and Phishing
- Spam: Unsolicited messages (usually ads).
- Phishing: Fake messages pretending to be legit to steal data.
## Social Engineering
- Manipulating people into giving up confidential info (e.g., pretending to be IT support).
## Password Attacks
- Cracking passwords via brute-force, dictionary attacks, or credential stuffing.
## Threats
- Anything that could cause harm (e.g., hacker, natural disaster).
## Vulnerabilities
- Weaknesses in a system (e.g., unpatched software).
## Exploits
- The use of a vulnerability to launch an attack.
## Risk
- The potential for damage when a threat uses a vulnerability.
## Web Security

---

## OWASP Top 10
- 10 most common and critical web app security risks (e.g., XSS, Injection).
## XSS (Cross-Site Scripting)
- Injecting malicious scripts into websites to run in users’ browsers.
## Injection Attack (e.g., SQLi)
- Sending malicious code (like SQL) through input fields to manipulate databases.
## CSRF (Cross-Site Request Forgery)
- Forcing users to perform unwanted actions when authenticated (e.g., changing email address without knowing).
## SSRF (Server-Side Request Forgery)
- Attacker tricks a server into making requests to internal systems.
## HTTP Header Smuggling
## Session Fixation
## Application Security
## Network Security
## How SSL/TLS works
## How DNS works
## TCP 3 way handshake
## Firewall
## DoS and DDoS
## Ping Flood
## Cache Poisoning

## Cloud Security

---

## Shared Responsibility
## IAM
## CSPM
## CASB
## CWPP
## Cryptography
## Encryption and Decryption
## Hashing
## Encoding and Decoding
## Salt
