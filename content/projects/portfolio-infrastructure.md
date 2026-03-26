---
title: "My Portfolio Infrastructure"
draft: false
---


How I built a containerized, high-performance portfolio using Hugo and Docker to ensure consistent deployments and secure web hosting.

---

## Project Impact & Core Functionality

This project moved beyond simple web design to focus on the infrastructure required to host a professional cybersecurity brand. By using Docker, I created an isolated environment that ensures the site runs identically on my local machine and the production server, eliminating "it works on my machine" errors. The final architecture serves as a low-latency, secure platform to showcase my technical labs and research.

---

## Technical Deep Dive: Problems & Fixes

### Problem 1: Port Collision & Ghost Processes

**The Problem:** During development, the Hugo server failed to start, returning a "Port 1313 already in use" error despite no visible windows being open.

**The Fix:** I used the lsof -i :1313 command to identify the Process ID (PID) of a background Hugo instance that failed to terminate. After running kill -9 [PID], the port was released, allowing the new container to bind to the host correctly.

### Problem 2: Docker Container Networking

**The Problem:** The site was running perfectly inside the Docker container, but when I navigated to localhost:1313 on my MacBook, the page wouldn't load.

**The Fix:** I realized I hadn't mapped the container's internal port to my machine's external port. I updated my Docker run command to include -p 1313:1313, successfully bridging the network gap between the isolated container and my browser.

### Problem 3: Theme Submodule Synchronization

**The Problem:** When I first pushed the site to GitHub, the homepage was blank because the PaperMod theme files were missing from the repository.

**The Fix:** I learned that Hugo themes are often managed as Git Submodules. I had to initialize and update the submodules using git submodule update --init --recursive to ensure the styling was correctly pulled into the deployment pipeline.

### Problem 4: Image Path Inconsistency

**The Problem:** Images for my security projects appeared locally but broke on the live site because of case-sensitive naming in the Linux-based Docker environment.

**The Fix:** I refactored the file structure to use strictly lowercase naming and corrected the baseURL in the config.toml file to match the GitHub Pages subdirectory.

### Problem 5: Manual Deployment Latency

**The Problem:** Every time I made a small text change, I had to manually rebuild the site and push files, which was slow and prone to human error.

**The Fix** I engineered a GitHub Actions workflow that automates the build process. Now, any change pushed to the main branch triggers an automatic Docker build and deployment, ensuring the site is always up to date.

### The Next Level: Hardening & Analytics

**Current State:** The site is live and updates automatically via CI/CD.

**The Risk:** Without monitoring, I have no visibility into potential attack attempts or how users are interacting with the project labs.

**The Plan:** In the next phase, I will integrate Google Analytics to track engagement.

---