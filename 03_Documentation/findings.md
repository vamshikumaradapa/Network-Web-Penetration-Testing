# Assessment Findings

## Overview

This document summarizes the findings identified during the penetration testing assessment of the **Metasploitable 2** virtual machine and **Damn Vulnerable Web Application (DVWA)**. The assessment included both network-level and web application security testing performed within a controlled laboratory environment.

A total of **10 security assessments** were completed. Several high and critical vulnerabilities were identified, demonstrating common security weaknesses found in intentionally vulnerable systems.

---

# Assessment Summary

| Attack No. | Assessment | Severity | Status |
|------------|------------|----------|--------|
| 1 | Reconnaissance (Nmap) | Informational | ✅ Completed |
| 2 | VSFTPD Assessment | Critical | ✅ Completed |
| 3 | SSH Authentication Assessment | High | ✅ Completed |
| 4 | Password Hash Analysis | High | ✅ Completed |
| 5 | Telnet Assessment | High | ✅ Completed |
| 6 | MySQL Assessment | High | ✅ Completed |
| 7 | SQL Injection | Critical | ✅ Completed |
| 8 | Cross-Site Scripting (XSS) | High | ✅ Completed |
| 9 | Command Injection | Critical | ✅ Completed |
| 10 | File Upload Vulnerability | Critical | ✅ Completed |

---

# Key Findings

## 1. Reconnaissance

The Nmap scan identified multiple open ports and exposed services, including FTP, SSH, Telnet, HTTP, MySQL, and SMB. This information was used to identify the target's attack surface.

**Severity:** Informational

---

## 2. VSFTPD Assessment

The FTP service was running **VSFTPD 2.3.4**, a version affected by a known backdoor vulnerability. Successful exploitation resulted in root-level access to the target machine.

**Severity:** Critical

---

## 3. SSH Authentication Assessment

Weak credentials were successfully identified using Hydra, allowing remote SSH login to the target system.

**Severity:** High

---

## 4. Password Hash Analysis

Password hashes extracted from the target system were successfully cracked using John the Ripper, demonstrating the use of weak passwords.

**Severity:** High

---

## 5. Telnet Assessment

The Telnet service transmitted authentication credentials in plain text. Wireshark packet capture confirmed that usernames and passwords could be intercepted by anyone monitoring the network.

**Severity:** High

---

## 6. MySQL Assessment

The MySQL service allowed remote access, enabling database enumeration and retrieval of user information stored in the DVWA database.

**Severity:** High

---

## 7. SQL Injection

The DVWA application was vulnerable to SQL Injection. User input manipulated SQL queries, allowing unauthorized retrieval of database information.

**Severity:** Critical

---

## 8. Cross-Site Scripting (XSS)

The application failed to sanitize user input, allowing JavaScript code to execute within the user's browser.

**Severity:** High

---

## 9. Command Injection

Unsanitized user input allowed arbitrary operating system commands to be executed on the target server.

**Severity:** Critical

---

## 10. File Upload Vulnerability

The application accepted and executed an uploaded PHP web shell, resulting in Remote Code Execution (RCE).

**Severity:** Critical

---

# Severity Distribution

| Severity | Count |
|----------|------:|
| Critical | 4 |
| High | 5 |
| Informational | 1 |
| Medium | 0 |
| Low | 0 |

---

# Overall Assessment

The penetration testing assessment revealed multiple high-impact vulnerabilities affecting both network services and web applications. Critical issues such as SQL Injection, Command Injection, unrestricted File Upload, and the vulnerable VSFTPD service demonstrated that an attacker could achieve unauthorized access and remote code execution.

Additionally, weak authentication mechanisms, insecure protocols like Telnet, and inadequate password management increased the overall attack surface. These findings emphasize the importance of secure configuration, strong authentication, encrypted communication, regular patching, and secure coding practices.

---

# Conclusion

The assessment successfully demonstrated common security vulnerabilities in a controlled laboratory environment. All identified issues were documented with supporting evidence and accompanied by recommendations to improve the overall security posture. This project provided practical experience in reconnaissance, vulnerability assessment, exploitation within an authorized environment, and professional technical reporting.