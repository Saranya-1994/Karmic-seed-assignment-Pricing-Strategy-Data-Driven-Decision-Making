# 📊 XYZ Company — Pricing Strategy Report
### Karmic Seed | Operations Analyst — Round 3 Assignment

---

## 🧾 Assignment Overview

This project presents a **data-driven pricing strategy** for XYZ Company, an eco-friendly tableware brand selling 50 SKUs on an online marketplace. The goal was to analyze six datasets and build a structured pricing framework that improves profitability while staying competitive.

---

## 🔍 Key Findings

| Metric | Value |
|--------|-------|
| Total SKUs Analyzed | 50 |
| SKUs Below Minimum Margin | 42 (84%) |
| Average Current Gross Margin | 12.1% |
| Average Projected Gross Margin | 23.3% |
| SKUs Recommended for Price Increase | 41 |
| SKUs Recommended to Hold | 9 |

### Critical Issues Identified
- **5 SKUs** (MN-05, MN-09, MN-18, MN-23, MN-30) operating at **negative gross margins**
- **27 SKUs** with ACoS > 30%, making advertising loss-making
- **4 SKUs** (MN-14, MN-15, MN-25, MN-29) with return rates above 15%
- **3 SKUs** in overstock (Days of Supply > 120) and **3 SKUs** at low stock risk

---

## 🧠 Methodology — Five-Factor Dynamic Pricing Model

The pricing framework applies five sequential adjustments in priority order:

```
Step 1 → Cost Floor Protection     (minimum acceptable margin = 20%)
Step 2 → Competitor Anchoring      (base price at 98% of avg competitor)
Step 3 → Inventory Adjustment      (±5% based on Days of Supply)
Step 4 → Return Rate Gate          (cap price if return rate > 15%)
Step 5 → ACoS Correction           (+3% nudge if ACoS > 30%)
```

### Pricing Formula
| Component | Formula |
|-----------|---------|
| Total Cost | COGS + FBA Fee + Storage Fee + Handling |
| Minimum Price | Total Cost ÷ (1 − Min Margin %) |
| Competitor Anchor | Avg Competitor Price × 0.98 |
| Inventory Adj. | Base × 0.95 (overstock) or × 1.05 (low stock) |
| Final Price | Rounded to nearest X.90 (psychological pricing) |

---

## 📁 Datasets Used

| Dataset | Description |
|---------|-------------|
| Pricing Data | SKU costs, current prices, FBA fees, storage fees |
| Competitor Data | Competitor price ranges per SKU |
| Sales Data | Units sold, conversion metrics |
| Inventory Data | Stock levels, Days of Supply |
| Ads Data | ACoS, ad spend, ad-attributed revenue |
| Returns Data | Return counts by SKU (7-day and 30-day) |

---

## 🗂️ Repository Structure

```
📦 xyz-pricing-strategy
 ┣ 📄 XYZ_Pricing_Strategy_Report_Updated.pdf   ← Final report (9 pages)
 ┣ 📄 README.md                                  ← This file
```

---

## 🛠️ Tools & Technologies

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![ReportLab](https://img.shields.io/badge/ReportLab-PDF-red?style=flat)

- **Python** — Data analysis and pricing logic
- **Pandas** — Data cleaning, transformation, and computation
- **ReportLab + pypdf** — PDF report generation and formatting

---

## 📌 Implementation Roadmap

| Timeline | Action |
|----------|--------|
| **Week 1** | Reprice 5 negative-margin SKUs immediately |
| **Weeks 2–3** | Raise prices for 36 underpriced SKUs in two tranches |
| **Week 4** | Operational review of high-return SKUs |
| **Month 2** | Monthly pricing refresh + ACoS bid optimization |
| **Quarter 2** | Build automated pricing tool (Python / Google Apps Script) |

---

## ⚠️ Key Assumptions & Limitations

- Conversion rates assumed stable within ±15% price movements
- Competitor prices are point-in-time — should be refreshed monthly
- Framework does not account for promotions, coupons, or lightning deals
- MN-17 return rate anomaly (`-` value) treated as zero
- Storage fee anomalies for MN-26 and MN-27 were cleaned during preprocessing

---

## 👤 Author
Saranya c j
**Operations Analyst Candidate**
Karmic Seed — Round 3 Assignment

---

> *This pricing framework is designed to be transparent, repeatable, and easy to implement in any standard spreadsheet tool.*

