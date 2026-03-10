# 🛸 How Secure Are Modern Drones?

> A multi-method cybersecurity research study analyzing real-world UAV vulnerabilities, regulatory landscapes, and manufacturer transparency.

---

## 📌 Project Overview

This project investigates the security posture of modern Unmanned Aerial Vehicles (UAVs) through systematic analysis of confirmed vulnerabilities, attack vectors, and manufacturer responses. Rather than theorizing about *possible* attacks, this research focuses on **what is actually being reported and exploited** in the wild.

The research was conducted as part of an academic course at **Université libre de Bruxelles (ULB)**, supervised by **Professor Jan Tobias Mühlberg**.

### Team Members

| Name | Student ID |
|---|---|
| Hiba Khadraoui | 000624402 |
| Oussama Ebn Atou | 000624234 |
| Zhang Enning | 000623725 |

---

## 🎯 Research Questions

1. What are the most common and most dangerous flaws in modern drones?
2. How do risks differ between consumer and professional drones?
3. What types of attacks threaten different drone applications most?
4. How effective are manufacturers' security responses?

---

## 🔬 Methodology

### Data Collection
We collected and analyzed **25 confirmed drone-related CVEs** (Common Vulnerabilities and Exposures) from the [NIST National Vulnerability Database (NVD)](https://nvd.nist.gov/), focusing on vulnerabilities reported between **2022 and 2024**.

### Classification Framework
Each CVE was categorized across four dimensions:

| Dimension | Categories Used |
|---|---|
| **Vulnerability Type** | Input validation, authentication bypass, buffer overflow, protocol flaws, weak credentials, race conditions |
| **Attack Vector** | Cyber-based, signal/hardware-based |
| **Severity Level** | High, Medium, Low |
| **Drone Category** | Consumer, Commercial, Enterprise/Software |

---

## 📊 Key Findings

### Finding #1 — Vulnerability Types
Input validation flaws are the single most common vulnerability class in modern drones:

- 🔴 **Input Validation Flaws** — 28%
- 🟠 **Authentication Bypass** — 20%
- 🟡 **Protocol & Buffer Issues** — 16% each
- ⚪ **Weak Credentials / Race Conditions** — remaining share

### Finding #2 — Consumer Drones Are Most Exposed
Consumer drones accounted for nearly half of all vulnerabilities found:

- **Consumer Drones** — 12 CVEs (48%)
- **Commercial Drones** — 8 CVEs (32%)
- **Enterprise / Software** — 5 CVEs (20%)

Consumer drones are disproportionately vulnerable due to weak default authentication, unencrypted communication channels, and a design-for-convenience-over-security philosophy.

### Finding #3 — Cyber Attacks Dominate
- **Cyber-based attacks** — 72% of all vulnerabilities
- **Signal/hardware attacks** (e.g., GPS spoofing, jamming) — 28%

### Finding #4 — Manufacturer Transparency Is Severely Lacking
- **Open-source platforms** (e.g., PX4) — 100% transparency
- **Major brands** (e.g., DJI) — ~40% transparency
- **Smaller companies** — 0% transparency

> Overall, only **40% of identified vulnerabilities had documented fixes**, leaving the majority of affected drones unpatched and exposed.

---

## 🌍 Regulatory Landscape

### European Union
| Regulation | Description |
|---|---|
| EU 2019/945 & 947 | Drone market and operational requirements |
| EN 4709-003 (Draft) | Cybersecurity technical standards |
| C0–C4 Class System | Risk-based categorization (mandatory since 2024) |
| U-space | Digital traffic management (2025–2026 rollout) |

**Gaps:** Cybersecurity requirements lack technical specificity. Remote ID lacks secure channels, creating spoofing risks. An activation lock proposal was rejected in 2025 over privacy concerns.

### United States
| Regulation | Description |
|---|---|
| 14 CFR Part 107 | Commercial drone operations |
| 14 CFR Part 89 | Remote ID Rule (effective 2021) |
| NIST SP 800-233 | Draft cybersecurity guidance (2024) |

**Approach:** Broadcast-only Remote ID with minimal mandated security. No required encryption or firmware security protocols.

### China
| Standard | Description |
|---|---|
| Interim Regulations (2024) | National UAV flight management framework |
| GB 46761–2025 | Real-name registration & hardware activation (effective May 2026) |
| GB 46750–2025 | Operational identification specification (effective May 2026) |

**Approach:** Hardware-level flight locks and continuous structured data reporting to a national platform — prioritizing unauthorized-use prevention over software vulnerability management.

> 🔍 **Key Insight:** The EU and China represent fundamentally different regulatory philosophies. The EU targets software lifecycle security; China enforces operational identity control. A combined approach addressing both would provide broader coverage.

---

## 📚 Papers & Sources Read

The following academic and institutional sources informed this research:

| # | Source | Relevance |
|---|---|---|
| 1 | Albarghouthi et al. (2013). *UFO: Verification with interpolants* | Formal verification background |
| 2 | Heron (2009). *Advanced Encryption Standard (AES)* | Encryption standards for UAV comms |
| 3 | Brown. *Drone Uses: The Awesome Benefits of Drone Technology* | Consumer drone adoption context |
| 4 | Civil Aviation Authority (2019). *Drone registration and education service* | Regulatory background |
| 5 | Bansod et al. (2017). *Satellite-based vs. drone-based remote sensing* | UAV applications landscape |
| 6 | Huang & Wang (2018). *Combating control signal spoofing in UAV systems* | Signal-layer attack mitigations |
| 7 | Zhang et al. (2019). *Detection of abnormal power emission in UAV networks* | Anomaly detection in drone comms |
| 8 | Sedjelmaci, Senouci & Ansari (2018). *Hierarchical detection against cyber-attacks in UAV networks* | Multi-layer security frameworks |
| 9 | Frew (2018). *An overview of new armed drone operators* | Threat actor landscape |
| 10 | Qiao, Zhang & Du (2017). *Vision-based GPS spoofing detection for small UAVs* | GPS spoofing countermeasures |
| 11 | Kerns et al. (2014). *Unmanned aircraft capture via GPS spoofing* | GPS spoofing attacks |
| 12 | Nassi et al. (2018). *Game of Drones: Detecting streamed POI from encrypted FPV* | Privacy and side-channel attacks |
| 13 | Pleban, Band & Creutzburg (2014). *Hacking and securing the AR.Drone 2.0* | Early consumer drone vulnerabilities |
| 14 | NIST NVD (n.d.). *Vulnerability search: DRONE* | Primary CVE data source |
| 15 | FAA (2021). *Remote identification of unmanned aircraft* (14 CFR Part 89) | US regulatory framework |
| 16 | NIST SP 800-233 Draft (2024). *Cybersecurity guidance for UAS* | US cybersecurity standards |
| 17 | CEN/CENELEC (2025). *EN 4709-003: Cybersecurity requirements for UAS* | EU technical standards |
| 18 | China SAMR & CAAC (2025). *GB 46761–2025 & GB 46750–2025* | Chinese drone standards |
| 19 | ASTM International (2022). *F3501-22: Minimum cybersecurity for UAS* | Industry baseline standards |
| 20 | ISO (in development). *ISO 23751: UAS Cybersecurity requirements* | International standardization |
| 21 | ITU (2023). *Security framework for UAS communications* | Global comms security standards |
| 22 | European Commission (2025). *U-space implementation roadmap 2.0* | EU airspace management |

---

## 🎤 Presentation

This research was presented before final publication. The slide deck covers the motivation, methodology, key findings, regulatory analysis, and recommendations.

📄 **[View Presentation Slides](./presentation/How_Secure_Are_Modern_Drones_choladeck.pptx)**

### Presentation Highlights
- Why security matters for cyber-physical systems like drones
- Live walkthrough of CVE analysis methodology
- Animated reveal of 4 key findings
- Comparative regulatory analysis: EU vs. US vs. China
- Conclusions and actionable recommendations

---

## 📁 Repository Structure

```
drone-security-research/
├── README.md                          # This file
├── paper/
│   └── How_Secure_Are_Modern_Drones.docx   # Full research paper
└── presentation/
    └── How_Secure_Are_Modern_Drones_choladeck.pptx  # Presentation slides
```

---

## 💡 Conclusions & Recommendations

Drone security is still **inconsistent and reactive**. Key takeaways:

- Consumer drones are disproportionately vulnerable due to weak defaults
- Cyber-based attacks represent the dominant and growing threat vector
- Most manufacturers — especially smaller ones — fail to disclose or patch vulnerabilities
- Regulatory frameworks address different threat dimensions and are not yet comprehensive

**Recommended actions:**
1. Strengthen industry-wide security baselines and standards
2. Mandate vulnerability disclosure and patch timelines
3. Improve default security configurations in consumer drone models
4. Encourage independent third-party security testing
5. Develop hybrid regulatory models combining operational identity controls with software-level resilience

---

## 🏫 Academic Context

- **Institution:** Université libre de Bruxelles (ULB)
- **Supervisor:** Prof. Jan Tobias Mühlberg
- **Research Period:** 2024–2025
- **Data Scope:** CVEs from NVD, 2022–2024

---

*This repository is part of an ongoing effort to document academic research and projects publicly.*
