---
title: "Offensive Security & Pentesting Lab"
draft: false
---

A segregated, high-fidelity virtual laboratory used to simulate the end-to-end lifecycle of a cyberattack to identify and mitigate defensive gaps.

---

## Project Impact & Core Functionality
This lab environment allowed for the safe execution of offensive security tactics against a hardened Linux target, bridging the gap between theoretical knowledge and technical application. By utilizing a Kali Linux attack vector, I successfully mapped the target's attack surface and executed a series of exploits to gain unauthorized access. The project concludes with a full post-exploitation analysis, demonstrating how weak service configurations and poor credential management lead to total system compromise.

---

## Technical Deep Dive: Problems & Fixes

### Problem 1: Reconnaissance Noise & Data Gaps

**The Problem:** Initial basic scans were easily detected by host-level logging and provided an incomplete picture of the target's network topology.

**The Fix:** I advanced my reconnaissance strategy by using Zenmap for visual topology mapping and dmitry for deep-dive subdomain and OSINT gathering. This provided a clearer "map" of the target before any exploit was attempted.

### Problem 2: Egress Filtering & Firewall Blocks

**The Problem:** Standard exploit attempts were being dropped by the target's firewall, which was configured to block unsolicited incoming connections on non-standard ports.

**The Fix:** I pivoted to a Reverse Shell payload using Metasploit. By forcing the victim machine to initiate the outbound connection to my Kali instance, I successfully bypassed the firewall's inbound filtering rules.

### Problem 3: Service-Level Vulnerabilities (vsFTPd)

**The Problem:** Identifying the entry point was difficult until I performed version-specific scanning on open services.

**The Fix:** I identified a known backdoor in the vsFTPd 2.3.4 service. I utilized the exploit/unix/ftp/vsftpd_234_backdoor module to trigger a root shell, gaining my first foothold on the system.

### Problem 4: Password Hash Obstacles

**The Problem:** Even with root access, several critical configuration files remained encrypted or password-protected, preventing full data exfiltration.

**The Fix:** I dumped the system's /etc/shadow files and used John the Ripper with a custom wordlist to perform an offline brute-force attack. This successfully cracked the local account hashes, proving the danger of weak password policies.

### Problem 5: Automated Detection "Noise"

**The Problem:** Relying on heavy frameworks like Metasploit generated significant forensic artifacts that would be easily caught by a modern EDR or SIEM like Splunk.

**The Fix:** I have begun replacing automated modules with custom Python and Bash scripts for manual exploitation. By "living off the land" and using native system binaries, I can maintain a lower profile and bypass automated security triggers that look for known exploit signatures.

### The Next Level: Defensive Integration

**Current State:** I can successfully breach and navigate a vulnerable Linux target.

**The Risk:** In a real-world scenario, an attacker's movement would eventually be flagged by an internal SOC team.

**The Plan:** I will integrate Splunk and Sysdig into the lab to monitor my own attack traffic. This "Purple Team" approach will allow me to see exactly which commands trigger alerts, helping me refine both my offensive stealth and defensive detection capabilities.

---