---
title: "About Me"
layout: "page"
---

<style>
    /* Hero Section - Vertical Alignment for better spacing */
    .profile-hero {
        text-align: center;
        padding: 40px 0;
        border-bottom: 1px solid var(--border);
        margin-bottom: 50px;
    }

    .profile-img {
        width: 160px;
        height: 160px;
        border-radius: 50%;
        object-fit: cover;
        object-position: 50% 15%;
        border: 3px solid #AB0520;
        margin-bottom: 25px;
        box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    }

    .profile-hero h1 {
        font-size: 3rem;
        margin: 0;
        color: var(--primary);
        letter-spacing: -1.5px;
    }

    .profile-hero .subtitle {
        font-size: 1.1rem;
        color: var(--secondary);
        margin-bottom: 30px;
    }

    .strategy-text {
        max-width: 800px;
        margin: 0 auto;
        font-size: 1.1rem;
        line-height: 1.7;
        color: var(--primary);
        text-align: center;
    }

    /* Impact Sections */
    .section-label {
        font-size: 1rem;
        font-weight: 700;
        color: var(--primary);
        text-transform: uppercase;
        letter-spacing: 1.5px;
        margin-bottom: 40px;
    }

    .content-wrapper {
        max-width: 850px;
        margin: 0 auto;
    }

    .exp-entry {
        margin-bottom: 45px;
    }

    .exp-title-bar {
        display: flex;
        justify-content: space-between;
        align-items: baseline;
    }

    .exp-entry h3 {
        margin: 0;
        font-size: 1.3rem;
        color: #AB0520;
        font-weight: 700;
    }

    .exp-line {
        width: 35px;
        height: 2px;
        background-color: #AB0520;
        margin: 8px 0 18px 0;
    }

    .exp-date {
        font-size: 0.9rem;
        color: var(--secondary);
    }

    .exp-body p {
        margin-bottom: 15px;
        line-height: 1.65;
    }

    /* Skills Table */
    .skills-grid {
        width: 100%;
        border-collapse: collapse;
        margin-top: 20px;
    }

    .skills-grid td {
        padding: 15px 0;
        border-bottom: 1px solid var(--border);
        vertical-align: top;
    }

    .skills-label {
        width: 25%;
        font-weight: 700;
        color: #AB0520;
    }
</style>

<div class="profile-hero">
    <img src="../img/profile.jpg" alt="Kyler Nats" class="profile-img">
    <h1>Kyler Nats</h1>
    <p class="subtitle">Cybersecurity Professional | M.S. in MIS</p>
    <div class="strategy-text">
        I specialize in bridging the gap between technical defense and business resilience. By aligning infrastructure deployment with organizational risk, I secure critical assets while maintaining the agility needed for innovation. I leverage a proactive break-fix methodology to identify and mitigate vulnerabilities before they become business liabilities, ensuring long-term system integrity and compliance.
    </div>
</div>

<div class="content-wrapper">
    <h2 class="section-label">Impact</h2>

    <div class="exp-entry">
        <div class="exp-title-bar">
            <h3>Enterprise Security Operations</h3>
            <span class="exp-date">FirstBank | Summer 2025</span>
        </div>
        <div class="exp-line"></div>
        <div class="exp-body">
            <p>Wrote comprehensive technical documentation for core security alerts and investigation workflows. This initiative is projected to reduce future analyst training and development time by 30%, ensuring a consistent and rapid response across the SOC.</p>
            <p>Led the integration of Nexus AI within Proofpoint. By transitioning from static, rule-based filtering to an AI-learned response model, I automated a historically manual triage process, saving analysts 25% of their weekly investigation time.</p>
            <p>Investigated alerts across a network of 2,500+ employees using Splunk and CrowdStrike, maintaining zero operational downtime by identifying risks before they escalated into incidents.</p>
        </div>
    </div>

    <div class="exp-entry">
        <div class="exp-title-bar">
            <h3>Risk Management & Compliance</h3>
            <span class="exp-date">University of Arizona, McKeever Lab | 2025 – Present</span>
        </div>
        <div class="exp-line"></div>
        <div class="exp-body">
            <p>Leading a comprehensive Information Security Risk Management (RMaP) project using the NIST 800-53 framework. This involves performing a gap analysis and implementing security controls within the UASecure platform.</p>
            <p>Established a hardened infrastructure that allows for federal research data to be processed with 100% adherence to university and grant-mandated security standards, moving beyond check-box compliance to functional security.</p>
        </div>
    </div>

    <div class="exp-entry">
        <div class="exp-title-bar">
            <h3>Data Analytics & Strategic Growth</h3>
            <span class="exp-date">UA Baseball Strategic Consultant | 2025 – Present</span>
        </div>
        <div class="exp-line"></div>
        <div class="exp-body">
            <p>Leading a team to process 14M+ data points, identifying key awareness leakages in the current marketing funnel to scale fan attendance and organizational revenue through advanced data modeling.</p>
            <p>Developed a data-driven strategy projected to increase organization revenue by 10% and scale attendance potential by 20% through targeted engagement and funnel optimization.</p>
        </div>
    </div>

    <h2 class="section-label">Technologies & Skills</h2>

    <table class="skills-grid">
        <tr>
            <td class="skills-label">Defensive Ops</td>
            <td>Splunk, CrowdStrike, Proofpoint Nexus AI, Nessus, Kali Linux</td>
        </tr>
        <tr>
            <td class="skills-label">Cloud & DevOps</td>
            <td>AWS, Terraform, Docker, Kubernetes, GitHub Actions</td>
        </tr>
        <tr>
            <td class="skills-label">Frameworks</td>
            <td>NIST 800-53, NIST CSF 2.0, CMMC 2.0, MITRE ATT&CK</td>
        </tr>
        <tr>
            <td class="skills-label">Data & Code</td>
            <td>Elasticsearch, Python, SQL, Linux CLI</td>
        </tr>
    </table>

    <h2 class="section-label" style="margin-top: 60px;">Education</h2>
    <p style="margin-bottom: 10px;"><strong>M.S. in Management Information Systems</strong> | University of Arizona | Expected May 2026</p>
    <p><strong>B.S. in Management Information Systems</strong> | University of Arizona | Magna Cum Laude</p>
</div>

