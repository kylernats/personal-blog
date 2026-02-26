---
title: "Offensive Security & Pentesting Lab"
draft: false
---

I built a dedicated virtual environment to practice the full lifecycle of a cyberattack, from initial reconnaissance to gaining root access.

**What I accomplished:**
I stood up a **Kali Linux** attack machine and targeted a vulnerable Linux server. I performed a full penetration test using industry-standard tools like **nmap**, **dmitry**, and **Nessus** to identify weak points, eventually using **Metasploit** to exploit a backdoor in the **vsFTPd** service.

**The Problem & The Fix**
* **The Problem:** My initial network scans were noisy and provided incomplete data.
* **The Fix:** I moved from basic **nmap** commands to using **Zenmap** for better visual topology mapping and **dmitry** for gathering information on subdomains and open ports. 
* **The Problem:** Even after finding an open port, a firewall was dropping my incoming exploit attempts.
* **The Fix:** I switched to a **Reverse Shell** payload. Instead of trying to force my way in, I made the victim machine initiate a connection back to my Kali instance. 
* **The Problem:** I found several password-protected files on the system that I couldn't access even with root.
* **The Fix:** I used **John the Ripper** to perform an offline brute-force attack on the hashes I dumped. By using a custom wordlist, I cracked the local account passwords and proved how easily weak credentials lead to a total system compromise.



**What I'd do differently next time:**
I want to practice more manual techniques. Instead of relying on big tools like Metasploit, I’d like to write my own custom Python or Bash scripts to exploit vulnerabilities. This would help me stay under the radar of automated security systems.

---
