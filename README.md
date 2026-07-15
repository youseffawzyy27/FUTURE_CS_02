# FUTURE_CS_02 — Phishing Email Detection & Awareness System

**Future Interns — Cyber Security Internship (Task 2)**
Candidate: Yousef Ahmed Fawzy
CIN ID: FIT/JUN26/CS9482
Internship Period: 29 June 2026 – 29 July 2026

---

## 📌 Overview

This project analyzes real-world phishing email samples to identify common phishing indicators,
classify their risk level, and produce a professional awareness report with prevention guidelines —
simulating the work of a security analyst conducting phishing detection and employee awareness training.

This is a **security education and analysis task** — no hacking, exploitation, or offensive actions were performed.

---

## 🎯 Objective

- Analyze real phishing email samples (headers, sender domains, links, content)
- Identify phishing indicators (spoofed senders, fake domains, malicious links)
- Classify each email's risk level: **Safe / Suspicious / Phishing**
- Explain each attack in simple, non-technical language
- Produce prevention tips and Do's/Don'ts guidelines for end users and employees

---

## 🛠️ Tools & Sources Used

- Manual raw header inspection (`.eml` source analysis)
- Browser-based rendered-view inspection (safe, non-interactive)
- Public phishing sample archive: [rf-peixoto/phishing_pot](https://github.com/rf-peixoto/phishing_pot) (GitHub) — used for study/reference only
- Public spam/ham research corpus: SpamAssassin public dataset
- Google Message Header Analyzer — toolbox.googleapps.com/apps/messageheader
- MxToolbox Email Header Analyzer — mxtoolbox.com/EmailHeaders.aspx

---

## 🔍 Analysis Approach

1. **Collect** — sourced real phishing/spam samples from verified public research archives
2. **Analyze Headers** — examined From, Reply-To, Return-Path, and Authentication-Results (SPF/DKIM)
3. **Inspect Domains & Links** — compared claimed brand domains against actual sending/link domains
4. **Identify Indicators** — compiled spoofing, authentication, and social-engineering red flags
5. **Classify Risk** — rated each sample Safe / Suspicious / Phishing based on cumulative evidence
6. **Document Findings** — compiled everything into a structured PDF report
7. **Prevention Guidelines** — produced actionable awareness guidance for users and employees

---

## 📁 Repository Structure

```
FUTURE_CS_02/
├── README.md
├── Evidence/
│   ├── sample1_microsoft_account_alert.eml
│   ├── sample2_bank_account_blocked.eml
│   ├── sample3_coinbase_fraud.eml
│   ├── sample3_coinbase_rendered.html
│   ├── sample4_insurance_marketing.eml
│   └── Screenshots/
│       ├── 01_sample1_rendered_view.png
│       ├── 02_sample1_raw_headers.png
│       ├── 01_sample2_rendered_view.png
│       ├── 02_sample2_raw_headers.png
│       ├── 01_sample3_rendered_view.png
│       ├── 02_sample3_raw_headers.png
│       ├── 01_sample4_rendered_view.png
│       └── 02_sample4_raw_headers.png
└── Report/
    └── FUTURE_CS_02_Phishing_Detection_Awareness_Report.pdf
```

---

## 📊 Summary of Findings

| Sample | Impersonated Brand | Key Red Flags | Risk Level |
|---|---|---|---|
| 1. Account Alert | Microsoft | Fake domain, mismatched Reply-To/Return-Path, no SPF/DKIM | 🔴 Phishing |
| 2. Bank Alert | Chase | Display spoofing, SPF/DKIM pass for wrong domain, shortened malicious link | 🔴 Phishing |
| 3. Crypto Alert | Coinbase | Filter-evasion naming, SPF/DKIM pass for wrong domain, disguised redirect link | 🔴 Phishing |
| 4. Marketing Ad | None (self-branded) | Bulk-mail infrastructure, no impersonation, no credential theft | 🟡 Suspicious |

**Key takeaway:** Passing SPF/DKIM checks does *not* mean an email is safe — these checks only confirm
an email came from the domain shown in its own headers, which can itself belong entirely to the attacker.

---

## 📄 Full Report

See [`Report/FUTURE_CS_02_Phishing_Detection_Awareness_Report.pdf`](./Report/FUTURE_CS_02_Phishing_Detection_Awareness_Report.pdf)
for the complete analysis, screenshots, header breakdowns, and prevention guidelines.

---

## ⚖️ Ethics & Scope Note

All samples analyzed were sourced from public, research-oriented archives specifically intended for
educational study. No live phishing links were clicked, no credentials were entered, and no content from
reference repositories was copied or reused — all indicators, analysis, and conclusions in this report are
original work.
