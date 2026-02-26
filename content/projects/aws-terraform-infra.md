
---
title: "Automated AWS Infrastructure with Terraform"
draft: false
---

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