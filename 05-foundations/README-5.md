# Course 5 — Assets, Threats & Vulnerabilities

**Platform:** Google Cybersecurity Professional Certificate, Coursera  
**Duration:** ~26 hours

---

## What This Course Covers

How to classify assets, identify threats and vulnerabilities, and apply frameworks to protect organizational data.

---

## Key Topics

### Asset Classification

| Level | Who Can Access | Example |
|-------|---------------|---------|
| **Restricted** | Need-to-know only | Trade secrets, patient records |
| **Confidential** | Limited, specific users | Financial reports, employee data |
| **Internal Only** | All employees | Company policies, internal memos |
| **Public** | Anyone | Marketing materials, public website |

### Threat Actor Types

| Type | Motivation | Example |
|------|-----------|---------|
| Nation-State | Espionage, disruption | APT groups |
| Cybercriminal | Financial gain | Ransomware gangs |
| Hacktivist | Political/social agenda | DDoS against corporations |
| Insider Threat | Revenge, money, accident | Disgruntled employee |
| Script Kiddie | Curiosity, fame | Using downloaded attack tools |

### Vulnerability Assessment

A vulnerability assessment finds weaknesses before attackers do. Steps:
1. **Identify** all systems in scope
2. **Scan** for known vulnerabilities (CVEs)
3. **Analyze** likelihood and impact
4. **Prioritize** using a risk score (Likelihood × Severity)
5. **Remediate** starting with highest priority

### OWASP Top 10 (Web Application Vulnerabilities)

| # | Vulnerability | What It Means |
|---|--------------|---------------|
| 1 | Broken Access Control | Users exceed their permissions |
| 2 | Cryptographic Failures | Weak/missing encryption exposes data |
| 3 | Injection | Malicious code inserted into application |
| 4 | Insecure Design | Security not built into the architecture |
| 5 | Security Misconfiguration | Default settings, open storage buckets |
| 6 | Vulnerable & Outdated Components | Unpatched open-source libraries |
| 7 | ID & Authentication Failures | Weak logins, no MFA |
| 8 | Software & Data Integrity Failures | Supply chain attacks (e.g. SolarWinds) |
| 9 | Security Logging & Monitoring Failures | Can't detect what you don't log |
| 10 | Server-Side Request Forgery (SSRF) | App fetches attacker-controlled URLs |

### Identity and Access Management (IAM)

**IAM** ensures: Right user → Right resource → Right time → Right reason

**SSO (Single Sign-On):** One login for multiple systems. Uses LDAP or SAML protocols.  
**MFA (Multi-Factor Authentication):** Requires 2+ factors (something you know + have + are)

**Access control models:**
- **MAC** (Mandatory Access Control) — Strictest; government/military use
- **DAC** (Discretionary Access Control) — Owner controls who accesses their files
- **RBAC** (Role-Based Access Control) — Access based on job role; most common in enterprise

---

## Skills Gained
`Asset classification` `Threat modeling` `Vulnerability assessment` `OWASP Top 10` `IAM` `SSO` `MFA` `RBAC` `Risk scoring` `CVE awareness`
