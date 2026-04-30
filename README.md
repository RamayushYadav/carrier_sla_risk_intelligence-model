# Enterprise B2B Supply Chain Analytics & Machine Learning Project
## Carrier Performance & SLA Risk Intelligence Platform

---

## 1. Project Overview
Modern B2B supply chains operate under high volatility, strict Service Level Agreements (SLAs), and rising cost pressure. Enterprises rely on third‑party logistics providers (3PLs) and carriers, yet most analytics remain **reactive**.

This project builds a **predictive, explainable, and enterprise‑grade intelligence platform** that proactively identifies carrier‑level and route‑level SLA breach risk before shipment execution.

---

## 2. Business Context
**Client (Simulated):** Apex Manufacturing Ltd.  
**Industry:** Manufacturing / Retail Distribution  
**Annual Logistics Spend:** USD 50–200 Million  
**Regions:** APAC, EMEA, AMER  
**Logistics Model:** Multi‑carrier outsourced transportation

### Key Stakeholders
- Head of Supply Chain – Overall SLA reliability
- Logistics Operations Manager – Daily execution & firefighting
- Procurement Head – Carrier contracts & negotiations
- Finance Controller – Cost & penalty exposure
- Customer Fulfillment Lead – Delivery experience

---

## 3. Business Problem
Traditional logistics dashboards answer **what happened**, not **what will happen**.

**Core Question:**
> Which carrier is likely to breach SLA on upcoming shipments, on which routes, and why?

This platform answers that question using predictive analytics and ML.

---

## 4. Objectives
### Primary Objective
- Predict SLA breach risk at shipment, carrier, route, and region level
- Enable proactive operational and procurement decisions

### Secondary Objectives
- Reduce SLA penalties
- Improve carrier accountability
- Balance cost vs reliability
- Improve customer experience

---

## 5. Solution Architecture

**This platform is:**
- Shipment‑level
- Feature‑engineered
- ML‑powered
- Explainable
- Business‑oriented

**This platform is NOT:**
- A static BI dashboard
- A black‑box ML model
- A toy Kaggle dataset

---

## 6. Dataset Overview
- **Rows:** ~200,000 shipments
- **Granularity:** 1 row = 1 shipment
- **Source:** Synthetic but enterprise‑realistic (ERP/TMS‑like)
- **File:** `data/b2b_carrier_sla_risk_intelligence_100k.csv`

---

## 7. Data Dictionary (MetaDataset)

| Column Name | Type | Description | Business Meaning |
|------------|------|-------------|------------------|
| shipment_id | String | Unique shipment ID | Audit & traceability |
| vendor | Categorical | Carrier name | Contract performance |
| shipping_mode | Categorical | Road / Sea / Air / Rail | Cost & risk driver |
| region | Categorical | APAC / EMEA / AMER | Macro risk context |
| origin_country | Categorical | Origin location | Route definition |
| destination_country | Categorical | Destination location | SLA sensitivity |
| weight_kg | Float | Shipment weight | Capacity & cost |
| volume_cbm | Float | Shipment volume | Load efficiency |
| fragile_flag | Binary | Fragile indicator | Handling risk |
| priority_flag | Binary | Priority shipment | SLA strictness |
| planned_delivery_days | Integer | SLA commitment | Contractual promise |
| actual_delivery_days | Integer | Actual transit time | Execution result |
| delivery_delay_days | Integer | Delay vs SLA | Risk indicator |
| shipping_cost_usd | Float | Shipment cost | Financial impact |
| sla_breach_flag | Binary | Delay > 0 | ML target |

---

## 8. Feature Engineering Strategy
Key engineered features include:
- Rolling carrier SLA breach rate (30/60/90 days)
- Route‑level volatility index
- Mode‑specific delay statistics
- Cost vs reliability ratios
- Carrier degradation trend score

These features transform raw logistics data into **risk intelligence**.

---

## 9. Machine Learning Problem
- **Type:** Binary Classification
- **Target:** `sla_breach_flag`
- **Goal:** Predict probability of SLA breach

### Models Used
- Logistic Regression (baseline)
- Random Forest
- Gradient Boosting
- XGBoost (optional)

---

## 10. Explainability & Trust
Enterprise adoption requires transparency.

This project includes:
- Feature importance analysis
- SHAP‑based explanations
- Business‑friendly reasoning
- Auditable predictions

---

## 11. Business Outputs

### Dashboards (Conceptual)
- Carrier Risk Heatmap
- Route × Mode Risk Matrix
- Cost vs Reliability Trade‑off
- SLA Breach Trends

### Decision Support
- Carrier selection recommendations
- Contract renegotiation insights
- Proactive rerouting alerts

---

## 12. Repository Structure

```text
carrier-sla-risk-intelligence/
│
├── data/
│   ├── raw/
│   │   └── b2b_carrier_sla_risk_intelligence_100k.csv
│   └── processed/
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_model_training.ipynb
│   └── 04_explainability_shap.ipynb
│
├── src/
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── model_training.py
│   ├── evaluation.py
│   └── explainability.py
│
├── dashboards/
│   └── bi_mockups/
│
├── reports/
│   └── business_insights.md
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## 13. Success Metrics
- Reduction in SLA breaches
- Lower penalty costs
- Faster risk detection
- Improved procurement decisions

---

## 14. Why This Is a Real B2B Project
- Clear buyer & users
- Predictive (not descriptive)
- Explainable ML
- Enterprise‑ready design
- Clear ROI focus

---

## 15. Future Enhancements
- Time‑series SLA forecasting
- Weather & port congestion signals
- Multi‑carrier optimization
- Real‑time streaming ingestion
- ERP / TMS integration

---

## 16. Conclusion
This project demonstrates how **data, machine learning, and business context** combine to deliver proactive supply chain intelligence. It moves beyond dashboards into **decision‑ready analytics**.

---

## Author
**Designed for Enterprise‑Grade Supply Chain Analytics & ML Portfolios**

