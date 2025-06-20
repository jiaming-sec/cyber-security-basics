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
- Sending specially crafted headers to bypass security controls between servers.
## Session Fixation
- Attacker sets a session ID and tricks the victim into using it, allowing hijack.

## Application Security
- Securing software apps from threats (input validation, patching, secure coding).
## Network Security
- Protecting data as it travels across networks (firewalls, IDS, VPN).
## How SSL/TLS works
- Encrypts data between browser ↔️ server using certificates (public/private keys).
## How DNS works
- Resolves human-readable domains (e.g., google.com) to IP addresses via DNS servers.
## TCP 3 way handshake
- Connection setup: SYN ➝ SYN-ACK ➝ ACK between client and server.
## Firewall
- Filters network traffic based on rules (blocks bad IPs, ports, protocols).
## DoS and DDoS
- Overwhelms a server to make it unavailable. DDoS uses multiple sources (botnet).
## Ping Flood
- A basic DoS using massive ICMP echo requests to flood a target.
## Cache Poisoning
- Inserting malicious data into a DNS cache so users are redirected to malicious sites.

## Cloud Security

---

## Shared Responsibility
- Cloud provider secures infrastructure; you secure your apps/data.
## IAM (Identity & Access Management)
- Manages user identities and what they can access.
## CSPM (Cloud Security Posture Management)
- Tools that detect misconfigurations in cloud environments.
## CASB (Cloud Access Security Broker)
- Enforces security policies between cloud service users and providers.
## CWPP (Cloud Workload Protection Platform)
- Secures workloads (e.g., containers, VMs) running in cloud environments.
## Cryptography
## Encryption and Decryption
## Hashing
## Encoding and Decoding
## Salt
