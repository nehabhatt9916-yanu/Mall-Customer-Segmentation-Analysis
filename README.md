 🛍️ Shopping Mall Customer Segmentation Analysis

> **Uncovering the truth that income doesn't drive spending — and what actually matters for retail strategy.**

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-4C72B0)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-orange)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Project Overview

This project is a **full-cycle customer segmentation analysis** on 15,079 shopping mall visitors. Using Python for EDA and K-Means clustering, plus a Power BI dashboard, the analysis reveals four behaviorally distinct customer segments — each nearly equal in size — and delivers actionable marketing strategies for each.

**The headline finding:** The Pearson correlation between annual income and spending score is **0.003** — statistically zero. Income is not a predictor of spending behavior in this dataset. This single insight reframes the entire marketing strategy.

---

## 📂 Repository Structure

```
mall-customer-segmentation/
│
├── 📓 notebooks/
│   └── Mall_customer_analysis.ipynb       # Full analysis notebook (EDA + segmentation + visuals)
│
├── 📊 data/
│   └── Shopping_Mall_Customer_Segmentation_Data.csv   # Raw dataset (15,079 records)
│
├── 🖼️ visuals/
│   ├── chart1_gender_distribution.png     # Gender pie chart
│   ├── chart2_age_distribution.png        # Age-wise bar chart
│   ├── chart3_income_vs_spending.png      # Scatter plot (near-zero correlation)
│   ├── chart4_segment_distribution.png    # Segment bar chart
│   └── chart5_segment_gender_boxplot.png  # Spending score by segment & gender
│
├── 📄 reports/
│   └── Mall_Customer_Segmentation_Report.pdf  # Full business report
│
├── requirements.txt                        # Python dependencies
└── README.md                               # This file
```

---

## 📊 Dataset Description

| Column | Type | Description |
|--------|------|-------------|
| `Customer ID` | String | Unique identifier (UUID format) — excluded from analysis |
| `Age` | Integer | Customer age (18–90 years) |
| `Gender` | String | Male / Female |
| `Annual Income` | Integer | Yearly income in Indian Rupees (₹20,022 – ₹1,99,974) |
| `Spending Score` | Integer | Mall-assigned score from 1–100 based on purchase behavior |

**Data Quality:** Zero null values. Zero duplicate rows. 100% complete dataset across all 15,079 records.

---

## 🔍 Key Findings

### 1. Customer Profile
| Metric | Value |
|--------|-------|
| Total Customers | 15,079 |
| Average Age | 54.19 years |
| Average Annual Income | ₹1,09,743 |
| Average Spending Score | 50.59 / 100 |
| Gender Split | 50.4% Male / 49.6% Female |

### 2. Income ≠ Spending (The Core Insight)

```
Pearson r (Income vs Spending Score) = 0.003
```

A customer earning ₹1.8 lakh is **no more likely** to spend highly than someone earning ₹30,000. Marketing strategies built on income targeting would miss more than half the high-spending population.

### 3. Age Group Spending Scores
| Age Band | Mean Spending Score |
|----------|---------------------|
| 18–25    | 51.84 ⬆ Highest     |
| 26–35    | 49.80 ⬇ Lowest      |
| 36–45    | 50.62               |
| 46–55    | 51.08               |
| 56–65    | 50.71               |
| 66+      | 50.27               |

The range is only ~2 points — the mall serves all life stages fairly equally.

### 4. Gender Has No Effect
- Male avg spending score: **50.78**
- Female avg spending score: **50.40**
- Gap of 0.38 points → statistically noise. Gender-split campaigns would be wasted effort.

---

## 🎯 Customer Segments

Using a **median split** on both income (₹1,09,190) and spending score (51):

| Segment | Headcount | % | Business Priority |
|---------|-----------|---|-------------------|
| 🟣 High Income – High Spending (HI-HS) | 3,827 | 25.38% | **IMMEDIATE** — protect & grow |
| 🔵 High Income – Low Spending (HI-LS) | 3,713 | 24.62% | **URGENT** — untapped wallet share |
| 🟢 Low Income – High Spending (LI-HS) | 3,741 | 24.81% | **IMPORTANT** — emotionally loyal |
| 🟠 Low Income – Low Spending (LI-LS) | 3,798 | 25.19% | **GRADUAL** — build habits first |

> **Why median and not mean?** The mean is pulled upward by a small number of very high earners, which would distort the boundary. Median is robust to extremes and creates a more balanced, fair split.

All four segments are nearly equal in size (~25% each) — this mall genuinely needs **four simultaneous strategies**, not a single focus group.

---

## 🚀 Strategic Recommendations

### 🟣 HI-HS — Protect Your Best Customers
- **Tiered membership programme** (Prestige → Elite → Pinnacle) with non-monetary perks: reserved parking, dedicated billing counters, priority sale entry
- **Personal shopping contact** for top 300–400 customers via WhatsApp
- **Closed-door brand preview evenings** (invitation-only) twice a year
- **Birthday/anniversary experiential gifts** — restaurant reservations, spa afternoons (not discount vouchers)

### 🔵 HI-LS — Convert the Hesitant
- **Exit kiosks** with 3-question friction surveys before spending on promotions
- **Category discovery sessions** — personal styling, cooking demos, fragrance consultations
- **Exclusive 48-hour Insider Sale** — personalised selection from stores they browsed but didn't buy
- **Concierge click-and-collect** — select via app, bagged in 30 minutes

### 🟢 LI-HS — Reward Emotional Loyalty
- **Zero-cost instalment option** at checkout for purchases above ₹2,000
- **Peer referral scheme** earning mall credits (not just discounts)
- **Time offers around salary credit dates** (1st and 15th of month) and festivals (Navratri, Diwali, Eid)
- **'Loyal Shopper of the Month'** recognition near the food court

### 🟠 LI-LS — Build the Habit of Visiting
- **Free Wi-Fi zones**, weekend children's workshops, community fitness classes, cultural events
- **First loyalty reward at very low threshold** — spend ₹300, unlock ₹50 food court credit
- **Affordable aspirational products** (under ₹500) placed near entrances
- **Auto-migrate** customers who cross spending score 51 into LI-HS track

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.10+ | Core analysis language |
| pandas | Data loading, cleaning, aggregation |
| NumPy | Numerical operations |
| Matplotlib | Base plotting |
| Seaborn | Statistical visualizations |
| scikit-learn | K-Means clustering validation |
| Power BI | Interactive business dashboard |

---

## ⚙️ Installation & Usage

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/mall-customer-segmentation.git
cd mall-customer-segmentation
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Notebook
```bash
jupyter notebook notebooks/Mall_customer_analysis.ipynb
```

Or run it non-interactively:
```bash
jupyter nbconvert --to notebook --execute notebooks/Mall_customer_analysis.ipynb
```

### 4. View the Power BI Dashboard
Open `Mall_Customer_Dashboard_final.pbix` in **Power BI Desktop** (free download from Microsoft).

---

## 📈 Visualizations Preview

| Chart | What It Shows |
|-------|--------------|
| Gender Distribution (Pie) | Near-equal 50.4% / 49.6% split |
| Age Distribution (Bar) | Even spread across 6 age bands; largest cohort is 66+ |
| Income vs Spending (Scatter) | Flat cloud pattern = near-zero correlation |
| Segment Distribution (Bar) | All four segments ~25% each |
| Spending by Segment & Gender (Box) | Male/female boxes overlap — gender doesn't matter within segments |

---

## 📋 Methodology Notes

**Why median split over K-Means for primary segmentation?**

K-Means was used as a validation step. The median-split approach was chosen as the primary method because:
1. It produces **directly interpretable** business segments (high/low income × high/low spending)
2. The near-zero income-spending correlation means K-Means on all features doesn't create clean behavioral clusters
3. Business teams can immediately act on and communicate the four quadrants without statistical background

**Why no feature scaling?**

Income (₹20K–₹2L) and Spending Score (1–100) are on very different scales. For the scatter analysis and correlation, no scaling is needed. The median split is scale-invariant.

---

## 🔄 Recommended Next Steps

1. **Re-run segmentation every 3 months** — customers move between segments as their life circumstances change (a student becomes a salaried professional; a retiree changes spending habits)
2. **Collect visit frequency data** — the 0.003 correlation suggests spending is driven by something beyond income; frequency of visits is the most likely candidate
3. **A/B test recommendations** — start with HI-LS segment (3,713 customers, highest potential uplift) using exit kiosk surveys vs. control group
4. **Add transaction-level data** — current dataset has one row per customer; basket-level data would enable store-mix and cross-sell analysis

---

## 👩‍💼 Author

**Neha Bhatt**
Business Analyst


---

## 📄 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

---

## 🙏 Acknowledgements

- Dataset: Shopping Mall Customer Segmentation (15,079 records)
- Toolchain: Python 3, pandas, matplotlib, seaborn, Power BI
- Analysis methodology inspired by RFM segmentation principles and retail analytics best practices
