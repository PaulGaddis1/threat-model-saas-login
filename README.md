# IT Threat Model — SaaS Login & Dashboard (Paul Gaddis)

**Author:** Paul Gaddis — UTSA Information Systems & Technology  
**Date:** November 2025  

This project documents a complete threat model and remediation plan for a fictional SaaS platform, *AcmeApp*, which includes a user login, dashboard, and payment integration.  
The goal is to demonstrate practical security analysis, OWASP Top 10 mapping, and prioritized risk mitigation — without performing active penetration testing.

---

## 🔍 Overview
**Purpose:** Identify and analyze common security threats in a SaaS login/dashboard workflow and propose mitigations aligned with industry best practices.

**Scope:**
- User login and authentication
- User dashboard (data access, profile management)
- API and database communication
- Payment gateway and OAuth integration

**Deliverables:**
- `report/Threat_Model_Report.md` — full written report  
- `report/Threat_Model_Report.pdf` — printable formatted report  
- `diagrams/data_flow.png` — visual data flow diagram  
- `README.md` — repository overview and documentation  

---

## ⚙️ Key Findings
| Threat | OWASP Mapping | Severity | Recommended Fix |
|--------|----------------|-----------|----------------|
| Weak Authentication | A07 – Identification & Auth Failures | High | MFA, rate limiting, lockout |
| Broken Access Control (IDOR) | A01 – Broken Access Control | High | Server-side checks, UUIDs |
| Injection (SQL/NoSQL) | A03 – Injection | High | Parameterized queries |
| XSS | A07 – Cross-Site Scripting | Medium | Output encoding, CSP |
| Sensitive Data Exposure | A02 – Cryptographic Failures | High | TLS, secure cookie flags |
| Third-party Integration Risk | Supply-chain / External Components | Medium | Scoped API keys, callback validation |

---

## 📊 Prioritized Remediation Plan
1. **Immediate (0–2 weeks):** Fix IDOR, enforce TLS, set secure cookie flags.  
2. **Short-term (2–8 weeks):** Add MFA, rate limiting, breached-password checks.  
3. **Mid-term (1–3 months):** Harden third-party integrations, add WAF rules, automate scanning in CI/CD.

---

## 💡 Skills Demonstrated
- Threat modeling & OWASP Top 10 analysis  
- Security architecture reasoning  
- Prioritization and remediation planning  
- Technical documentation & report writing  

---

## 📄 Résumé / Portfolio Summary
Performed a threat model and remediation plan for a SaaS login/dashboard (AcmeApp), identifying six security risks mapped to OWASP Top 10 and recommending prioritized mitigations including MFA, access control hardening, and secure session handling.

---

## 🧠 Notes
This project focuses on **security design and analysis**, not active exploitation.  
All content and diagrams were created for educational and portfolio purposes by **Paul Gaddis** (UTSA — Information Systems & Technology).
