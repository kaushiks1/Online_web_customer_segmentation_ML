# Web Analytics Customer Segmentation using K-Means

## Project Overview

This project applies **K-Means clustering** to segment online website customers using realistic digital analytics and ecommerce behaviour data.

The objective is to help digital, product, marketing, and analytics teams identify actionable customer groups for:

- Conversion rate optimization
- Remarketing and retention
- Personalization
- Campaign targeting
- Customer journey improvement
- Revenue growth strategy

This is designed as a senior-level **Data Analyst / Data Scientist / Digital Analytics** portfolio project.

---

## Business Problem

A website receives thousands of visitors from different acquisition channels and devices. Not all customers behave the same way.

Some users are loyal and high-value, some research products but do not convert, some respond strongly to discounts, and others are low-engagement visitors.

The business question is:

> How can we segment website customers based on behavioural data and design better marketing and product strategies for each group?

---

## Dataset

The dataset is synthetic and designed to look realistic for a web analytics / ecommerce environment.

Rows: **6,000 customers**

File:

```text
data/web_customer_analytics_6000.csv
```

Key fields include:

- Sessions
- Pageviews
- Average session duration
- Bounce rate
- Product views
- Cart additions
- Transactions
- Revenue
- Days since last visit
- Email clicks
- Traffic source
- Device type
- Conversion rate
- Engagement score

A data dictionary is available here:

```text
data/data_dictionary.csv
```

---

## Methodology

1. Load customer-level website analytics data.
2. Select behavioural, ecommerce, engagement, and recency features.
3. Scale numerical variables using `StandardScaler`.
4. Evaluate K values using elbow method and silhouette score.
5. Fit final K-Means model.
6. Profile each cluster based on revenue, engagement, conversion, and recency.
7. Translate clusters into business recommendations.

---

## Folder Structure

```text
web_customer_segmentation_kmeans/
│
├── data/
│   ├── web_customer_analytics_6000.csv
│   └── data_dictionary.csv
│
├── notebooks/
│   └── customer_segmentation_kmeans.ipynb
│
├── src/
│   └── customer_segmentation_kmeans.py
│
├── reports/
│   ├── k_selection_metrics.csv
│   ├── segment_profile.csv
│   ├── customers_with_segments.csv
│   └── figures/
│       ├── elbow_method.png
│       ├── silhouette_scores.png
│       └── customer_segments_pca.png
│
├── docs/
│   └── project_summary.md
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## How to Run

```bash
pip install -r requirements.txt
python src/customer_segmentation_kmeans.py
```

---

## Key Outputs

| Output | Description |
|---|---|
| `segment_profile.csv` | Aggregated profile of each customer segment |
| `customers_with_segments.csv` | Full dataset with assigned K-Means segment |
| `k_selection_metrics.csv` | Elbow and silhouette metrics |
| `customer_segments_pca.png` | 2D visualization of clusters |
| `elbow_method.png` | Elbow method chart |
| `silhouette_scores.png` | Silhouette score chart |

---

## Business Recommendations

### High Value Loyal Customers

Retain through loyalty benefits, early access, premium bundles, and personalized product recommendations.

### Product Researchers

Use comparison content, product reviews, remarketing, and stronger calls-to-action to improve conversion.

### Deal-Driven Converters

Use controlled discounting and margin-aware campaigns. Avoid over-discounting customers who may convert without offers.

### Engaged Non-Buyers

Improve checkout UX, test basket recovery, and personalize recommendations based on browsing patterns.

### Low Engagement / At-Risk Visitors

Reduce inefficient retargeting spend and focus on low-cost reactivation campaigns.

---

## Tools Used

Python, Pandas, NumPy, Scikit-learn, Matplotlib, K-Means, PCA, Web Analytics, Customer Segmentation

---

## Author

Kaushik Somashekar  
Digital Analyst | Product Analyst | Data Analyst | Aspiring Data Scientist
