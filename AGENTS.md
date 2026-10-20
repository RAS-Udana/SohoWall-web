# AGENTS.md

Rules for any agent or contributor working on this project website.

## Project

**SOHOWALL — A Multi-Layered Intelligent Firewall Architecture for SOHO Networks**

- Project ID: R26-CS-017
- Course: IT4010 Research Project 2026, Faculty of Computing, SLIIT
- Supervisor: Mr. Amila Senarathne
- Co-Supervisor: Dr. Harinda Fernando

## Modules

All four modules are equal contributions. Give them the same visual weight.

| Module (title · subtitle) | Member | Student ID | Scope |
|---|---|---|---|
| M1 Threat Intelligence & Enforcement · *CTI IOC scoring with ML fallback and guarded enforcement* | Sakila Udana (Group Leader) | IT22233912 | Captures DNS, TLS SNI and TCP-flag metadata with Scapy. CTI IOC scoring (URLhaus, ThreatFox, Feodo Tracker) with ATT&CK-derived severity, feed corroboration and freshness, and an ML-ensemble **fallback** that runs only when no feed has a record. Sends features to M2 and block/unblock requests to M4 over HTTP. Does **not** write iptables/hosts rules. |
| M2 Anomaly Detection · *TinyML multi-layer network anomaly detection* | Dilshara N.P.G.R. | IT22064790 | Standalone TinyML autoencoder microservice (`monitor.py`) that scores windowed features from M1 and returns an anomaly score to M1's dashboard. |
| M3 Data Loss Prevention · *PII detection with FHE-protected risk scoring* | Pathiranage M.D. | IT22100252 | Transformer PII detection and PII-type models; risk scores kept under FHE (Microsoft SEAL, BFV); Flask logging and admin monitoring. |
| M4 Natural Language Firewall · *Plain-English rule generation and management API* | Dulanjana E.J.A.T. | IT22186874 | Plain English to iptables + /etc/hosts sinkhole rules (DistilBERT, Flan-T5 + LoRA, regex fallback), SQLite audit trail, token-protected API that fails closed. |

## Equal weighting

- Do not label any single module as "the main novelty" or "core innovation".
- Do not give one module a featured card, gradient border or extra section that the others lack.
- Do show who built which module (About Us and each module page); the guideline and individual marking need it. Keep the styling equal.

## Content rules

- Never invent results, dates or marks. Use `TODO` where information is missing.
- Never mention Dempster-Shafer or Raspberry Pi.
- Never say M3 is integrated with M4.
- Never describe M1 as writing iptables or hosts rules; M1 requests enforcement from M4 over HTTP.

## Technical rules

- Plain HTML + CSS only. No frameworks, no npm, no JavaScript.
- All paths relative.
- Whole site folder under 20 MB.
- Images in `.webp` or `.svg` only, each under 200 KB.
- Documents and slides are links only. Do not add the files to the site.

## Navigation

- Every page has the same tabs, in this order:
  **Home, Domain, Milestones, Documents, Presentations, About Us, Contact Us**
- Same header and footer on every page.
- Highlight the current page's tab.

## Design

- Dark only.
- Colours:
  - Background: `#05070D`
  - Cards: background `rgba(255,255,255,0.03)`, border `rgba(255,255,255,0.08)`
  - Text: `#F5F7FA` (primary), `#94A3B8` (secondary)
  - Accent gradient: `#22D3EE` to `#6366F1`, used sparingly
- Fonts:
  - Headings: Space Grotesk
  - Body: Inter
  - Labels: JetBrains Mono
- Max content width: 1200px.
- Calm and premium. No stock photos, no padlock clipart.
