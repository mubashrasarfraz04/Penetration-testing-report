# 🏥 Mediroza General Hospital - Penetration Testing Report
### 📅 Week 4 - Final Assessment Report

> 🔐 **A complete authorized Penetration Testing Report on Mediroza General Hospital Web Application, covering vulnerabilities, evidence, exploitation and remediation.**

![Status](https://img.shields.io/badge/Status-Completed-success)
![Week](https://img.shields.io/badge/Week-4-blue)
![Type](https://img.shields.io/badge/Type-Penetration%20Testing-red)
![Platform](https://img.shields.io/badge/Platform-Web%20Application-orange)

---

## 📋 Table of Contents
- [🎯 Project Overview](#-project-overview)
- [🏥 Target Information](#-target-information)
- [🔍 Scope of Testing](#-scope-of-testing)
- [🛠️ Tools Used](#️-tools-used)
- [⚠️ Vulnerabilities Found](#️-vulnerabilities-found)
- [📸 Evidence Collected](#-evidence-collected)
- [🛡️ Recommendations](#️-recommendations)
- [📊 Risk Summary](#-risk-summary)
- [📁 Report File](#-report-file)
- [👩‍💻 Author](#-author)
- [⚖️ Disclaimer](#️-disclaimer)

---

## 🎯 Project Overview

This repository contains the **Week 4 Final Penetration Testing Report** for the **Mediroza General Hospital** web application.

The goal of this assessment was to identify security weaknesses in the hospital's patient portal, admin panel, and lab report system that could expose sensitive patient and staff data.

**Testing Type:** 🖤 Black Box Penetration Testing  
**Duration:** 📅 Week 4  
**Environment:** 🧪 Authorized Lab / Testing Environment

---

## 🏥 Target Information

| Field | Details |
| :--- | :--- |
| **🏥 Application Name** | Mediroza General Hospital |
| **🌐 Application Type** | Hospital Management / Patient Portal |
| **👤 User Roles Tested** | Patient, Admin, Staff |
| **🔑 Login Portal** | Patient Portal Sign-In / Sign-Up |
| **📄 Main Features** | Lab Reports, Patient Records, Admin Panel |

---

## 🔍 Scope of Testing

✅ **In Scope:**
- 🔐 Patient Portal Login / Sign-Up Page
- 📄 My Lab Reports Dashboard
- 👨‍⚕️ Admin Panel & Password Management
- 🗄️ Database Backup & File Exposure
- 🔑 Password Security & Hash Analysis

❌ **Out of Scope:**
- 🚫 Physical Security Testing
- 🚫 Social Engineering / Phishing
- 🚫 Denial of Service (DoS) Attacks
- 🚫 Third-party Services

---

## 🛠️ Tools Used

| 🧰 Tool | 🎯 Purpose |
| :--- | :--- |
| **🌐 Browser** | Manual Testing & Navigation |
| **🦈 Burp Suite** | Intercepting Requests & Analyzing Traffic |
| **🔓 Hashcat** | Password Hash Cracking |
| **#️⃣ Hash Calculator** | Hash Identification & Analysis |
| **🔎 Nmap** | Port & Service Scanning |
| **🕷️ OWASP ZAP** | Vulnerability Scanning |

---

## ⚠️ Vulnerabilities Found

### 🔴 1. Critical - Exposed Database Backup File
- 📂 Sensitive backup file was publicly accessible.
- 👥 Contained staff usernames and password hashes.
- **Impact:** Full database compromise.

### 🔴 2. Critical - Weak Passwords Cracked
- 🔓 Password hashes were successfully cracked using Hashcat.
- 🔑 Weak passwords allowed unauthorized access.
- **Impact:** Admin / Staff account takeover.

### 🟠 3. High - Sensitive Patient Data Exposure
- 📄 Lab Reports were accessible without proper authorization.
- 🏥 Patient medical records were exposed.
- **Impact:** Privacy violation / Data breach.

### 🟠 4. High - Insecure Admin Password Reset
- 🔄 Admin panel allowed password reset without proper verification.
- **Impact:** Privilege escalation.

### 🟡 5. Medium - Information Disclosure in Login Page
- ℹ️ Login page revealed sensitive system information.
- **Impact:** Helps attacker in further exploitation.

---

## 📸 Evidence Collected

> ⚠️ **Note:** All sensitive data like passwords, usernames and personal information have been **redacted** for security.

1.  **Figure 1:** 🏠 Homepage of Mediroza General Hospital - Target application for testing.
2.  **Figure 2:** 🔐 Patient Portal Sign-In Page - Allows patients to access their medical records.
3.  **Figure 3:** 📄 Lab Reports page accessible after login - Sensitive patient data exposed.
4.  **Figure 4:** 🧪 Patient lab reports dashboard showing accessible medical records.
5.  **Figure 5:** #️⃣ Password hash captured for offline cracking analysis.
6.  **Figure 6:** 🔓 Password successfully cracked using Hashcat - Password redacted for security.
7.  **Figure 7:** 🗄️ Exposed database backup file containing staff credentials - Data redacted.
8.  **Figure 8:** 🛡️ Evidence of unauthorized access to internal system - Sensitive data redacted.

---

## 🛡️ Recommendations

- [ ] 🔒 **Remove** all publicly accessible backup files immediately.
- [ ] 🔑 **Enforce Strong Password Policy** - Minimum 12 characters, special characters.
- [ ] 🧂 **Use Strong Hashing** - Use bcrypt / Argon2 with salt, not MD5 / SHA1.
- [ ] ✅ **Implement MFA** - Multi-Factor Authentication for Admin & Staff.
- [ ] 🔐 **Fix Authorization** - Lab reports should only be visible to authorized patient.
- [ ] 🛡️ **Secure Admin Panel** - Add verification for password reset.
- [ ] 🔄 **Rotate All Credentials** - Change all exposed passwords immediately.
- [ ] 📝 **Regular Security Audits** - Conduct pentest every 3 months.

---

## 📊 Risk Summary

| Severity | Count | Color |
| :--- | :--- | :--- |
| 🔴 Critical | 2 | High Risk |
| 🟠 High | 2 | Medium-High Risk |
| 🟡 Medium | 1 | Medium Risk |
| **Total** | **5** | **Needs Immediate Action** |

---

## 📁 Report File

📄 **Full Detailed Report:** `Mediroza-Penetration-Testing-Report-Week-4.pdf`

> The PDF contains full methodology, screenshots, step-by-step exploitation, and detailed remediation steps.

---

## 👩‍💻 Author

**Mubashra**  
🎓 Cybersecurity Student | Penetration Tester  
🔗 LinkedIn:  https://www.linkedin.com/in/mubashra-khan-981805430?utm_source=share_via&utm_content=profile&utm_medium=member_android
🐙 GitHub: https://github.com/mubashrasarfraz04/Week-3-Password-Cracking/blob/main/README.md

---

## ⚖️ Disclaimer

> ⚠️ This penetration testing was performed **for educational purposes only** in an **authorized testing environment**. Do not attempt to test any live system without proper written permission. The author is not responsible for any misuse of this information.

---

⭐ **If you found this report helpful, please give it a star!** ⭐
