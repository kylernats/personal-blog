---
title: "My Portfolio Infrastructure"
draft: false
---


Building this site was a lesson in modern deployment and network troubleshooting.

**What I accomplished:**
I set up a professional portfolio using **Hugo** and **Docker** to show my work in a clean, secure way.

**The Problem & The Fix**
* **The Problem:** I tried to launch the site but it wouldn't load. My terminal said **Port 1313** was already in use.
* **The Fix:** I had to find what was occupying that port. I used a terminal command to find the process ID of a ghost Hugo process that hadn't shut down properly. Once I killed that process, the site loaded instantly.

**What I'd do differently next time:**
I'd set up a **CI/CD pipeline**. Right now I'm manually pushing files, but I'd love for the site to automatically update the second I save a new project in VS Code.

---