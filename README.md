# Information Security Risk Assessment: Kestrel Outdoor Ltd (fictional)

A risk assessment and ISO/IEC 27001:2022 gap analysis for a fictional UK online retailer, following the risk process in ISO/IEC 27001 clause 6.1 and ISO/IEC 27005 guidance.

> **Note:** Kestrel Outdoor Ltd is a made-up company created for this exercise. Built with AI assistance (Claude).

## What's in this repo
| File | Contents |
|---|---|
| [`Kestrel_Risk_Assessment_Report.pdf`](Kestrel_Risk_Assessment_Report.pdf) | Board-level report: executive summary, heat maps, top risks, ISO 27001 gap analysis, 6-month roadmap |
| [`Kestrel_Risk_Register.xlsx`](Kestrel_Risk_Register.xlsx) | Working register: assets, scoring method, risk register with live formulas, heat maps, gap analysis, treatment plan |

## The scenario
An 80-person online outdoor-gear retailer with about 150,000 customer accounts, a website on AWS, Microsoft 365, an on-premises warehouse system, an outsourced IT provider and a hosted payment page (PCI DSS SAQ A).

## Method
- 12 critical assets identified, each with an owner
- Threats, vulnerabilities and existing controls recorded for each risk
- Likelihood (1–5) × impact (1–5), with defined scales tied to money, outage time and personal data
- Treatment chosen (treat, transfer, avoid, accept) and residual risk re-scored against a stated risk appetite
- Each risk mapped to ISO/IEC 27001:2022 Annex A controls; 24 relevant controls assessed for gaps

## Key findings
- **4 Critical and 6 High risks** before treatment; **none above Medium** after the 18-action plan
- 11 of 24 relevant Annex A controls not implemented, 13 partly implemented
- Several quick wins are features the company already pays for but hasn't switched on (MFA, device encryption)

| ID | Risk | Inherent | Treatment | Residual | Owner |
|---|---|---|---|---|---|
| R01 | Ransomware encrypts warehouse server and backups | 20 Critical | Treat | 8 Medium | IT Manager |
| R02 | Business email compromise leads to invoice fraud | 16 Critical | Treat | 8 Medium | Finance Director |
| R09 | Unsupported warehouse server is exploited | 16 Critical | Treat | 8 Medium | IT Manager |
| R05 | AWS credentials leaked or misused | 15 Critical | Treat | 5 Medium | Lead Developer |
| R08 | Warehouse server failure stops dispatch | 12 High | Treat | 6 Medium | Operations Director |
| R12 | Customer accounts taken over through credential stuffing | 12 High | Treat | 6 Medium | Head of E-commerce |
| R13 | Slow or poor response to a security incident | 12 High | Treat | 6 Medium | IT Manager |
| R03 | Customer data exposed by a cloud misconfiguration | 10 High | Treat | 5 Medium | Head of E-commerce |
| R04 | Checkout tampering (e-skimming) redirects customers to a fake payment page | 10 High | Treat | 5 Medium | Head of E-commerce |
| R06 | Managed IT provider's remote access is compromised | 10 High | Treat | 5 Medium | IT Manager |
| R10 | Lost or stolen laptop exposes customer data | 9 Medium | Treat | 3 Low | IT Manager |
| R11 | Former employees keep access | 9 Medium | Treat | 3 Low | Head of People |
| R14 | Denial-of-service attack takes the website down during peak sales | 8 Medium | Accept | 8 Medium | Head of E-commerce |
| R07 | Breach at the email marketing supplier exposes customer emails | 6 Medium | Transfer | 4 Low | Marketing Manager |

## Frameworks and regulations referenced
ISO/IEC 27001:2022 · ISO/IEC 27005 · UK GDPR and Data Protection Act 2018 · PCI DSS (SAQ A)
