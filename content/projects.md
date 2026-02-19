---
title: "Security Projects"
date: 2026-02-19
draft: false
---

## Project 1: Offensive Security & Pentesting Lab
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

## Project 2: Automated AWS Infrastructure with Terraform
I wanted to build my labs using code instead of clicking through the AWS console. 

**What I accomplished:**
I wrote scripts to build a **VPC**, private subnets, and an **EC2 instance** from scratch.

**The Problem & The Fix**
* **The Problem:** My server was running, but I couldn't SSH into it. I had the pipes but no water flowing because I forgot to link my **Route Table** to the subnet.
* **The Fix:** I added a route table association block to my code. This finally allowed traffic to flow from the internet gateway to my server.
* **The Problem:** I originally had my secret AWS keys typed right into the files, which is a massive security risk.
* **The Fix:** I moved those secrets into **Environment Variables** so they never touched my GitHub account.

**What I'd do differently next time:**
I’d set up a **Bastion Host**. Right now my server is technically on the public internet so I can reach it, but in a real company, I'd want that server hidden in a private subnet with a jump box as the only way in.

---

## Project 3: Scalable RAG Chatbot Architecture
I designed a pipeline to help a chatbot pull real-time data from a massive Amazon dataset.

**What I accomplished:**
I built a **RAG (Retrieval-Augmented Generation)** system that lets an AI search through product data to find specific answers.

**The Problem & The Fix**
* **The Problem:** The dataset was so big that my server kept running out of memory and crashing.
* **The Fix:** I started using **DuckDB**. Instead of downloading the whole file, I streamed just the specific parts I needed from the cloud, cutting memory usage by 80%.
* **The Problem:** I didn't want my database sitting out in the open where anyone could try to log in.
* **The Fix:** I put the database inside a **VPC**. Now, only my own API can talk to it, and it’s completely invisible to the public internet.

**What I'd do differently next time:**
I'd look into using **Serverless Functions** for data processing. It would save money because the server would only turn on when new data arrives, rather than running 24/7.

---

## Project 4: My Portfolio Infrastructure
Building this site was a lesson in modern deployment and network troubleshooting.

**What I accomplished:**
I set up a professional portfolio using **Hugo** and **Docker** to show my work in a clean, secure way.

**The Problem & The Fix**
* **The Problem:** I tried to launch the site but it wouldn't load. My terminal said **Port 1313** was already in use.
* **The Fix:** I had to find what was occupying that port. I used a terminal command to find the process ID of a ghost Hugo process that hadn't shut down properly. Once I killed that process, the site loaded instantly.

**What I'd do differently next time:**
I'd set up a **CI/CD pipeline**. Right now I'm manually pushing files, but I'd love for the site to automatically update the second I save a new project in VS Code.

---