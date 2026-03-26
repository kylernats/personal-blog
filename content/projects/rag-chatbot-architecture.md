---
title: "Scalable RAG Chatbot Architecture"
draft: false
---

I built a high-performance Retrieval-Augmented Generation (RAG) pipeline designed to securely query massive datasets using vector embeddings and cloud-native architecture.

---

## Project Impact & Core Functionality

This project engineered a scalable solution for AI-driven data retrieval, allowing a chatbot to provide accurate, source-backed answers from a sprawling Amazon product dataset. By moving away from local file processing and implementing a DuckDB streaming architecture, I ensured the system could handle enterprise-scale data without crashing under memory constraints. The final architecture is fully isolated within a VPC, ensuring that sensitive data remains invisible to the public internet while remaining highly accessible to the internal API.

---

## Technical Deep Dive: Problems & Fixes

### Problem 1: Memory Overload & System Crashes

**The Problem:** The Amazon dataset was so massive that attempting to load the entire file into the server's RAM caused immediate system crashes.

**The Fix:** I implemented DuckDB to transition from full-file loading to a streaming architecture. By querying only the specific data chunks required for the RAG process, I reduced the server's memory footprint by 80%.

### Problem 2: Database Exposure & Security

**The Problem:** Initially, the database was sitting in a public subnet, making it a target for unauthorized login attempts and potential data breaches.

**The Fix:** I refactored the infrastructure to place the database inside a Private Subnet within a VPC. I configured specific Security Groups so that only my internal API can communicate with the data, effectively hiding it from the public internet.

### Problem 3: Inefficient "Always-On" Compute Costs

**The Problem:** The data processing server was running 24/7, even when no new data was being ingested, leading to unnecessary cloud costs.

**The Fix:** I proposed a move to Serverless Functions (such as AWS Lambda) for the ingestion pipeline. This ensures compute resources only activate when new data arrives, significantly lowering operational overhead.

### Problem 4: Inaccurate AI Hallucinations

**The Problem:** Without a strict retrieval mechanism, the chatbot would often make up product details that weren't in the actual dataset.

**The Fix:** I integrated a Vector Database to index the Amazon data into high-dimensional embeddings. This allows the system to retrieve only the most relevant facts before generating a response, ensuring every answer is grounded in factual evidence.

### Problem 5: Data Latency in Search

**The Problem:** Searching through millions of rows of raw text for every user query was too slow for a real-time chat interface.

**The Fix:** I implemented semantic search using specialized embedding models. This allows the system to understand the intent behind a user's question and find the correct data in milliseconds, rather than performing slow keyword matches.

### The Next Level: Production Hardening

**Current State:** The RAG system is functional, secure, and memory-efficient.

**The Risk:** In a production environment, prompt injection attacks could potentially trick the AI into leaking sensitive database information.

**The Plan:** In the next iteration, I will implement prompt guardrails to strictly validate all AI inputs and outputs, ensuring the system remains compliant with security standards like NIST 800-53.

---
