---
title: "About Me"
layout: "page"
---

<style>
    /* Header Section - Name and Subtitle */
    .about-header {
        padding-top: 40px;
        margin-bottom: 20px;
    }

    .about-header h1 {
        font-size: 3rem;
        margin: 0;
        color: var(--primary);
        letter-spacing: -1.5px;
        text-align: left;
    }

    .about-header .subtitle {
        font-size: 1.15rem;
        color: var(--secondary);
        margin: 8px 0 0 0;
        font-weight: 400;
        text-align: left;
    }

    /* Side-by-Side Grid for Photo and Paragraph */
    .content-grid {
        display: grid;
        grid-template-columns: 220px 1fr;
        gap: 60px;
        align-items: start; /* ALIGNS TOP OF PHOTO WITH TOP OF TEXT */
        padding-bottom: 50px;
        border-bottom: 1px solid var(--border);
        margin-bottom: 50px;
    }

    .profile-photo {
        width: 220px;
        height: 220px;
        min-width: 220px;
        border-radius: 50%;
        object-fit: cover;
        object-position: 50% 15%;
        border: 3px solid #AB0520;
        box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }

    .value-statement {
        font-size: 1.1rem;
        line-height: 1.7;
        color: var(--primary);
        margin: 0; /* Ensures no top margin pushes text down */
    }

    /* Mobile view - Stack centered */
    @media (max-width: 800px) {
        .about-header {
            text-align: center;
        }
        .about-header h1, .about-header .subtitle {
            text-align: center;
        }
        .content-grid {
            grid-template-columns: 1fr;
            justify-items: center;
            text-align: center;
            gap: 30px;
        }
    }

    /* Experience Styling */
    .section-label {
        font-size: 1rem;
        font-weight: 700;
        color: var(--primary);
        text-transform: uppercase;
        letter-spacing: 1.5px;
        margin: 50px 0 35px 0;
    }

    .exp-item {
        margin-bottom: 45px;
    }

    .exp-header {
        display: flex;
        justify-content: space-between;
        align-items: baseline;
    }

    .exp-header h3 {
        margin: 0;
        font-size: 1.35rem;
        color: #AB0520;
        font-weight: 700;
    }

    .exp-line {
        width: 35px;
        height: 2px;
        background-color: #AB0520;
        margin: 10px 0 20px 0;
        opacity: 0.8;
    }

    .exp-date {
        font-size: 0.95rem;
        color: var(--secondary);
    }

    .exp-text p {
        margin-bottom: 15px;
        line-height: 1.65;
    }

    /* Skills Table */
    .skills-table {
        width: 100%;
        border-collapse: collapse;
        margin-bottom: 60px;
    }

    .skills-table td {
        padding: 15px 0;
        border-bottom: 1px solid var(--border);
        vertical-align: top;
    }

    .skills-cat {
        width: 25%;
        font-weight: 700;
        color: #AB0520;
    }
</style>

<div class="about-header">
    <h1>Kyler Nats</h1>
    <p class="subtitle">Cybersecurity Professional | M.S. in MIS</p>
</div>

<div class="content-grid">
    <img src="../img/profile.jpg" alt="Kyler Nats" class="profile-photo">
    <div class="value-statement">
        I specialize in bridging the gap between technical defense and business resilience. By aligning infrastructure deployment with organizational risk, I secure critical assets while maintaining the agility needed for innovation. I leverage a proactive break-fix methodology to identify and mitigate vulnerabilities before they become business liabilities, ensuring long-term system integrity and compliance.
    </div>
</div>

<h2 class="section-label">Impact</h2>

<div class="exp-item">
    <div class="exp-header">
        <h3>Enterprise Security Operations</h3>
        <span class="exp-date">FirstBank | Summer 2025</span>
    </div>
    <div class="exp-line"></div>
    <div class="exp-text">
        <p>Wrote comprehensive technical documentation for core security alerts and investigation workflows. This initiative is projected to reduce future analyst training and development time by 30%, ensuring a consistent and rapid response across the SOC.</p>
        <p>Led the integration of Nexus AI within Proofpoint. By transitioning from static, rule-based filtering to an AI-learned response model, I automated a historically manual triage process, saving analysts 25% of their weekly investigation time.</p>
        <p>Investigated alerts across a network of 2,500+ employees using Splunk and CrowdStrike, maintaining zero operational downtime by identifying risks before they escalated into incidents.</p>
    </div>
</div>

<div class="exp-item">
    <div class="exp-header">
        <h3>Risk Management & Compliance</h3>
        <span class="exp-date">University of Arizona, McKeever Lab | 2025 – Present</span>
    </div>
    <div class="exp-line"></div>
    <div class="exp-text">
        <p>Leading a comprehensive Information Security Risk Management (RMaP) project using the NIST 800-53 framework. This involves performing a gap analysis and implementing security controls within the UASecure platform.</p>
        <p>Established a hardened infrastructure that allows for federal research data to be processed with 100% adherence to university and grant-mandated security standards, moving beyond check-box compliance to functional security.</p>
    </div>
</div>

<div class="exp-item">
    <div class="exp-header">
        <h3>Data Analytics & Strategic Growth</h3>
        <span class="exp-date">UA Baseball Strategic Consultant | 2025 – Present</span>
    </div>
    <div class="exp-line"></div>
    <div class="exp-text">
        <p>Leading a team to process 14M+ data points, identifying key awareness leakages in the current marketing funnel to scale fan attendance and organizational revenue through advanced data modeling.</p>
        <p>Developed a data-driven strategy projected to increase organization revenue by 10% and scale attendance potential by 20% through targeted engagement and funnel optimization.</p>
    </div>
</div>

<h2 class="section-label">Technologies & Skills</h2>

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

<h2 class="section-label" style="margin-top: 50px;">Education</h2>
<p style="margin-bottom: 10px;"><strong>M.S. in Management Information Systems</strong> | University of Arizona | Expected May 2026</p>
<p><strong>B.S. in Management Information Systems</strong> | University of Arizona | Magna Cum Laude</p>

