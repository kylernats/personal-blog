---
title: "Scalable RAG Chatbot Architecture"
draft: false
---


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
