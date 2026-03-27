---
title: "About Me"
layout: "page"
---

<style>
    .profile-header {
        display: flex;
        align-items: center;
        gap: 30px;
        margin-bottom: 40px;
    }
    .profile-pic {
        width: 180px;
        height: 180px;
        border-radius: 12px;
        object-fit: cover;
        border: 2px solid #AB0520;
    }
    .profile-intro h1 { margin: 0; color: var(--primary); }
    .profile-intro p { font-size: 1.1rem; color: var(--secondary); margin: 5px 0 15px 0; }
    
    .value-card {
        background: var(--card-bg, #f9f9f9);
        border-left: 5px solid #AB0520;
        padding: 20px;
        margin: 20px 0;
    }
    
    .experience-block { margin-bottom: 40px; }
    .experience-header { 
        display: flex; 
        justify-content: space-between; 
        align-items: baseline;
        border-bottom: 1px solid var(--border);
        padding-bottom: 5px;
        margin-bottom: 15px;
    }
    .experience-header h3 { margin: 0; color: #AB0520; font-size: 1.3rem; }
    .experience-date { font-size: 0.9rem; color: var(--secondary); font-style: italic; }
    
    .tech-pill {
        display: inline-block;
        padding: 4px 12px;
        background: #eee;
        border-radius: 20px;
        font-size: 0.8rem;
        margin: 0 5px 5px 0;
        color: #333;
    }
</style>

<div class="profile-header">
    <img src="../img/profile.jpg" alt="Kyler Nats" class="profile-pic">
    <div class="profile-intro">
        <h1>Kyler Nats</h1>
        <p>Cybersecurity Professional | M.S. in MIS</p>
        <div class="value-card">
            I specialize in bridging the gap between technical defense and business resilience. By aligning infrastructure deployment with organizational risk, I secure critical assets while maintaining the agility needed for innovation. I leverage a proactive break-fix methodology to identify and mitigate vulnerabilities before they become business liabilities, ensuring long-term system integrity and compliance.
        </div>
    </div>
</div>

## Strategic Impact

<div class="experience-block">
    <div class="experience-header">
        <h3>Enterprise Security Operations</h3>
        <span class="experience-date">FirstBank | Summer 2025</span>
    </div>
    <p>Wrote comprehensive technical documentation for core security alerts and investigation workflows. This initiative is projected to reduce future analyst training and development time by 30%, ensuring a consistent and rapid response across the SOC.</p>
    <p>Led the integration of Nexus AI within Proofpoint. By transitioning from static, rule-based filtering to an AI-learned response model, I automated a historically manual triage process, saving analysts 25% of their weekly investigation time.</p>
    <p>Investigated alerts across a network of 2,500+ employees using Splunk and CrowdStrike, maintaining zero operational downtime by identifying risks before they escalated into incidents.</p>
</div>

<div class="experience-block">
    <div class="experience-header">
        <h3>Risk Management & Compliance</h3>
        <span class="experience-date">University of Arizona, McKeever Lab | 2025 – Present</span>
    </div>
    <p>Leading a comprehensive Information Security Risk Management (RMaP) project using the NIST 800-53 framework. This involves performing a gap analysis and implementing security controls within the UASecure platform.</p>
    <p>Established a hardened infrastructure that allows for federal research data to be processed with 100% adherence to university and grant-mandated security standards, moving beyond check-box compliance to functional security.</p>
</div>

<div class="experience-block">
    <div class="experience-header">
        <h3>Data Analytics & Strategic Growth</h3>
        <span class="experience-date">UA Baseball Strategic Consultant | 2025 – Present</span>
    </div>
    <p>Leading a team to process 14M+ data points, identifying key awareness leakages in the current marketing funnel to scale fan attendance and organizational revenue through advanced data modeling.</p>
    <p>Developed a data-driven strategy projected to increase organization revenue by 10% and scale attendance potential by 20% through targeted engagement and funnel optimization.</p>
</div>

## Technologies & Skills

| Category | Tools & Technologies |
| :--- | :--- |
| **Defensive Ops** | Splunk, CrowdStrike, Proofpoint Nexus AI, Nessus, Kali Linux |
| **Cloud & DevOps** | AWS, Terraform, Docker, Kubernetes, GitHub Actions |
| **Frameworks** | NIST 800-53, NIST CSF 2.0, CMMC 2.0, MITRE ATT&CK |
| **Data & Code** | Elasticsearch, Python, SQL, Linux CLI |

## Education

* **M.S. in Management Information Systems** | University of Arizona | Expected May 2026
* **B.S. in Management Information Systems** | University of Arizona | Magna Cum Laude
