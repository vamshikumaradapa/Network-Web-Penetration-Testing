# Lab Setup

## Overview

This document describes the laboratory environment used for the **Metasploitable 2 Penetration Testing Lab**. The environment was designed to provide a safe and isolated platform for performing penetration testing exercises against intentionally vulnerable systems. All testing activities were conducted within a local virtual network to ensure that no production systems or external networks were affected.

---

# Laboratory Components

The lab environment consisted of two virtual machines hosted on Oracle VirtualBox.

| Component | Description |
|----------|-------------|
| Host Operating System | Windows 11 |
| Virtualization Platform | Oracle VirtualBox |
| Attacker Machine | Kali Linux (Latest Version) |
| Target Machine | Metasploitable 2 |
| Web Application | Damn Vulnerable Web Application (DVWA) |
| Network Configuration | Host-Only Network |

---

# Virtual Machine Configuration

## Kali Linux (Attacker)

| Parameter | Value |
|----------|-------|
| Operating System | Kali Linux (Latest Version) |
| Role | Attacker Machine |
| Purpose | Penetration Testing |
| Network Adapter | Host-Only Adapter |

---

## Metasploitable 2 (Target)

| Parameter | Value |
|----------|-------|
| Operating System | Metasploitable 2 |
| Role | Target Machine |
| Purpose | Vulnerability Assessment |
| Network Adapter | Host-Only Adapter |

---

# Network Configuration

Both virtual machines were connected using a **Host-Only Network** to create an isolated penetration testing environment.

| Device | IP Address |
|---------|------------|
| Kali Linux | 192.168.56.102 |
| Metasploitable 2 | 192.168.56.101 |

The Host-Only network allows communication between the virtual machines while preventing access from external networks, ensuring that all testing remains within the laboratory.

---

# DVWA Configuration

The **Damn Vulnerable Web Application (DVWA)** was used to perform web application security testing.

| Setting | Value |
|---------|-------|
| Web Application | DVWA |
| Security Level | Low |
| Access Method | Firefox Browser |
| URL | http://192.168.56.101/dvwa |

---

# Tools Installed

The following tools were used during the penetration testing assessment.

- Kali Linux
- Oracle VirtualBox
- Nmap
- Metasploit Framework
- Hydra
- John the Ripper
- Wireshark
- MySQL Client
- Firefox Browser
- DVWA

---

# Laboratory Architecture

```text
                    Windows 11 Host
                           │
                    Oracle VirtualBox
                           │
          ┌────────────────┴────────────────┐
          │                                 │
 ┌────────────────────┐           ┌────────────────────┐
 │     Kali Linux     │           │  Metasploitable 2  │
 │   Attacker Machine │◄────────►│    Target Machine   │
 └────────────────────┘ Host-Only └────────────────────┘
                                      │
                                      ▼
                   Damn Vulnerable Web Application (DVWA)
```

---

# Laboratory Workflow

The penetration testing assessment followed the workflow below:

1. Configure the virtual machines.
2. Verify network connectivity.
3. Perform reconnaissance using Nmap.
4. Assess vulnerable network services.
5. Test web application vulnerabilities using DVWA.
6. Collect screenshots and evidence.
7. Document findings and recommendations.

---

# Verification

Before starting the assessment, connectivity between the attacker and target machines was verified.

Example command:

```bash
ping 192.168.56.101
```

Successful replies confirmed that the attacker machine could communicate with the target machine.

---

# Summary

The laboratory environment provided a secure and isolated platform for performing penetration testing exercises. Using Kali Linux, Metasploitable 2, and DVWA within Oracle VirtualBox enabled practical experience with network reconnaissance, vulnerability assessment, password auditing, and web application security testing while ensuring that all activities remained within an authorized educational environment.