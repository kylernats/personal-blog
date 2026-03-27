---
title: "About Me"
layout: "page"
---

<style>
    /* Direct consistency with Homepage Hero */
    .about-hero {
        display: flex;
        align-items: center;
        gap: 40px;
        padding: 40px 0;
        border-bottom: 1px solid var(--border);
        margin-bottom: 40px;
    }

    .about-headshot {
        width: 160px;
        height: 160px;
        border-radius: 50%;
        object-fit: cover;
        object-position: 50% 15%;
        border: 3px solid #AB0520;
        box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }

    .about-info h1 {
        font-size: 3rem;
        margin: 0;
        color: var(--primary);
        letter-spacing: -1.5px;
    }

    .about-info p.subtitle {
        font-size: 1.1rem;
        color: var(--secondary);
        margin-top: 5px;
    }

    .value-statement {
        margin-top: 20px;
        font-size: 1.05rem;
        line-height: 1.6;
        color: var(--primary);
        max-width: 750px;
    }

    /* Section Headers */
    .section-title {
        font-size: 1.1rem;
        font-weight: 700;
        color: var(--primary);
        text-transform: uppercase;
        letter-spacing: 1px;
        margin: 40px 0 25px 0;
        border-bottom: 1px solid var(--border);
        padding-bottom: 10px;
    }

    /* Experience Items */
    .exp-item {
        margin-bottom: 35px;
    }

    .exp-row {
        display: flex;
        justify-content: space-between;
        align-items: baseline;
        margin-bottom: 10px;
    }

    .exp-row h3 {
        margin: 0;
        font-size: 1.2rem;
        color: #AB0520;
    }

    .exp-date {
        font-size: 0.9rem;
        color: var(--secondary);
    }

    .exp-text p {
        margin-bottom: 12px;
        line-height: 1.6;
        color: var(--primary);
    }

    /* Skills Table */
    .skills-table {
        width: 100%;
        border-collapse: collapse;
    }

    .skills-table td {
        padding: 12px 0;
        border-bottom: 1px solid var(--border);
        vertical-align: top;
    }

    .skills-cat {
        width: 25%;
        font-weight: 700;
        color: #AB0520;
    }
</style>

<div class="about-hero">
    <img src="../img/headshot.jpg" alt="Kyler Nats" class="about-headshot">
    <div class="about-info">
        <h1>Kyler Nats</h1>
        <p class="subtitle">Cybersecurity Professional | M.S. in MIS</p>
        <div class="value-statement">
            I specialize in bridging the gap between technical defense and business resilience. By aligning infrastructure deployment with organizational risk, I secure critical assets while maintaining the agility needed for innovation. I leverage a proactive break-fix methodology to identify and mitigate vulnerabilities before they become business liabilities, ensuring long-term system integrity and compliance.
        </div>
    </div>
</div>

<h2 class="section-title">Strategic Impact</h2>

<div class="exp-item">
    <div class="exp-row">
        <h3>Enterprise Security Operations</h3>
        <span class="exp-date">FirstBank | Summer 2025</span>
    </div>
    <div class="exp-text">
        <p>Wrote comprehensive technical documentation for core security alerts and investigation workflows. This initiative is projected to reduce future analyst training and development time by 30%, ensuring a consistent and rapid response across the SOC.</p>
        <p>Led the integration of Nexus AI within Proofpoint. By transitioning from static, rule-based filtering to an AI-learned response model, I automated a historically manual triage process, saving analysts 25% of their weekly investigation time.</p>
        <p>Investigated alerts across a network of 2,500+ employees using Splunk and CrowdStrike, maintaining zero operational downtime by identifying risks before they escalated into incidents.</p>
    </div>
</div>

<div class="exp-item">
    <div class="exp-row">
        <h3>Risk Management & Compliance</h3>
        <span class="exp-date">University of Arizona, McKeever Lab | 2025 – Present</span>
    </div>
    <div class="exp-text">
        <p>Leading a comprehensive Information Security Risk Management (RMaP) project using the NIST 800-53 framework. This involves performing a gap analysis and implementing security controls within the UASecure platform.</p>
        <p>Established a hardened infrastructure that allows for federal research data to be processed with 100% adherence to university and grant-mandated security standards, moving beyond check-box compliance to functional security.</p>
    </div>
</div>

<div class="exp-item">
    <div class="exp-row">
        <h3>Data Analytics & Strategic Growth</h3>
        <span class="exp-date">UA Baseball Strategic Consultant | 2025 – Present</span>
    </div>
    <div class="exp-text">
        <p>Leading a team to process 14M+ data points, identifying key awareness leakages in the current marketing funnel to scale fan attendance and organizational revenue through advanced data modeling.</p>
        <p>Developed a data-driven strategy projected to increase organization revenue by 10% and scale attendance potential by 20% through targeted engagement and funnel optimization.</p>
    </div>
</div>

<h2 class="section-title">Technologies & Skills</h2>

<table class="skills-table">
    <tr>
        <td class="skills-cat">Defensive Ops</td>
        <td>Splunk, CrowdStrike, Proofpoint Nexus AI, Nessus, Kali Linux</td>
    </tr>
    <tr>
        <td class="skills-cat">Cloud & DevOps</td>
        <td>AWS, Terraform, Docker, Kubernetes, GitHub Actions</td>
    </tr>
    <tr>
        <td class="skills-cat">Frameworks</td>
        <td>NIST 800-53, NIST CSF 2.0, CMMC 2.0, MITRE ATT&CK</td>
    </tr>
    <tr>
        <td class="skills-cat">Data & Code</td>
        <td>Elasticsearch, Python, SQL, Linux CLI</td>
    </tr>
</table>

<h2 class="section-title">Education</h2>
<p><strong>M.S. in Management Information Systems</strong> | University of Arizona | Expected May 2026</p>
<p><strong>B.S. in Management Information Systems</strong> | University of Arizona | Magna Cum Laude</p>