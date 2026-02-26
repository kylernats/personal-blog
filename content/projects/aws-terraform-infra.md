
---
title: "Automated AWS Infrastructure with Terraform"
draft: false
---

A technical deep-dive into replacing manual cloud configuration with a secure, immutable Infrastructure-as-Code (IaC) pipeline to deploy hardened AWS environments.

---

## Project Impact & Core Functionality

This project transitioned a manual workflow into a repeatable, version-controlled architecture, ensuring that every security group rule and subnet association is documented as code. By architecting a custom Virtual Private Cloud (VPC), I established a baseline for secure cloud operations that eliminates the risks of manual misconfiguration. The result is a functional, hardened web server environment that serves as the scalable foundation for future security labs.

## Technical Deep Dive: Problems & Fixes

### Problem 1: Subnet Connectivity

**The Problem:** After running terraform apply, the EC2 instance was running, but I could not ping or SSH into it despite having an Internet Gateway.

**The Fix:** I discovered that the subnet was not explicitly linked to the route table pointing to the Internet Gateway. I added an aws_route_table_association block to resolve the routing conflict.

### Problem 2: Credential Security

**The Problem:** I originally hardcoded my AWS Access Keys and Secret Keys directly into the .tf files, which is a security risk if pushed to GitHub.

**The Fix:** I refactored the provider block to use Environment Variables. This ensures credentials stay in the local terminal session and never touch the version control system.

### Problem 3: SSH Access Control

**The Problem:** Initially, my Security Group allowed SSH traffic (Port 22) from 0.0.0.0/0, leaving the server vulnerable to brute-force attempts from any IP.

**The Fix:** I modified the ingress rule to allow traffic only from my specific home IP address. This restricted the management interface to a single authorized source.

### Problem 4: Instance Bootstrapping

**The Problem:** The server launched with a default OS, requiring manual updates and tool installations after every deployment.

**The Fix:** I implemented a user_data script within the Terraform resource to automatically run yum update -y and install security tools during the initial boot.

### Problem 5: State File Management

**The Problem:** Running Terraform from different directories caused resource duplication and state conflicts.

**The Fix:** I moved the Terraform State to an S3 Backend. This established a "Single Source of Truth" for the infrastructure that is accessible from any management device.

### The Next Level: Bastion Host Architecture

**Current State:** The server is in a public subnet to allow for direct management.

**The Risk:** Even with IP-restricted Security Groups, a public-facing server remains a target for automated scanning.

**The Plan:** In the next iteration, I will move the primary server to a Private Subnet with no direct route to the internet. I will deploy a Bastion Host in the public subnet as the singular, monitored entry point for SSH traffic to meet enterprise security standards.

---