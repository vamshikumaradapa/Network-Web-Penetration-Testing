# Assessment Methodology

## Overview

This document describes the methodology followed during the penetration testing assessment of the **Metasploitable 2** virtual machine. The assessment was conducted in a structured and systematic manner within an isolated laboratory environment using **Kali Linux** as the attacker machine and **Metasploitable 2** as the target. The objective was to identify, verify, and document security vulnerabilities while following ethical penetration testing practices.

---

# Penetration Testing Process

The assessment was divided into five major phases:

1. Reconnaissance
2. Enumeration
3. Vulnerability Assessment
4. Exploitation
5. Documentation and Reporting

---

# Phase 1 – Reconnaissance

The first phase focused on collecting information about the target system. Network scanning was performed to identify active hosts, open ports, running services, service versions, and operating system details.

### Tool Used

- Nmap

### Activities Performed

- Host discovery
- Port scanning
- Service version detection
- Operating system detection
- Network service identification

### Outcome

A complete list of exposed services was obtained, providing the foundation for the remaining assessment phases.

---

# Phase 2 – Enumeration

Once active services were identified, enumeration was performed to gather detailed information about each service.

### Services Assessed

- FTP
- SSH
- Telnet
- SMB
- MySQL
- HTTP

### Activities Performed

- Service identification
- Authentication testing
- User enumeration
- Database enumeration
- Version verification

### Outcome

Enumeration identified several vulnerable services that required further security assessment.

---

# Phase 3 – Vulnerability Assessment

Each identified service was evaluated for known security weaknesses using industry-standard penetration testing tools.

### Network Security Assessment

- FTP Service Assessment
- SSH Authentication Assessment
- Password Hash Analysis
- Telnet Assessment
- MySQL Assessment

### Web Application Security Assessment

- SQL Injection
- Cross-Site Scripting (XSS)
- Command Injection
- File Upload Vulnerability

### Outcome

Multiple vulnerabilities were successfully identified and verified within the controlled laboratory environment.

---

# Phase 4 – Exploitation

Where appropriate and within the authorized lab environment, vulnerabilities were validated through controlled exploitation to demonstrate their security impact.

### Activities Performed

- Password authentication testing
- Password hash analysis
- Remote service access verification
- SQL Injection testing
- JavaScript injection testing
- Operating system command execution
- File upload validation

### Outcome

The exploitation phase confirmed the existence of several high and critical severity vulnerabilities.

---

# Phase 5 – Documentation and Reporting

Evidence collected throughout the assessment was organized into a structured technical report.

### Documentation Included

- Commands used
- Test procedures
- Screenshots
- Observations
- Risk assessment
- Security recommendations

### Outcome

A comprehensive penetration testing report was prepared to document the findings and recommended remediation measures.

---

# Assessment Workflow

```text
Lab Preparation
       │
       ▼
Reconnaissance
       │
       ▼
Enumeration
       │
       ▼
Vulnerability Assessment
       │
       ▼
Controlled Exploitation
       │
       ▼
Evidence Collection
       │
       ▼
Risk Assessment
       │
       ▼
Security Recommendations
       │
       ▼
Final Report
```

---

# Ethical Considerations

All penetration testing activities described in this project were conducted within an isolated virtual laboratory using intentionally vulnerable systems. No unauthorized systems, production environments, or third-party networks were targeted. The assessment was performed solely for educational purposes, cybersecurity skill development, and professional portfolio creation.

---

# Summary

The methodology followed a structured penetration testing lifecycle consisting of reconnaissance, enumeration, vulnerability assessment, controlled exploitation, and documentation. This approach ensured that the assessment was organized, repeatable, and aligned with professional penetration testing practices while maintaining ethical and authorized testing standards.