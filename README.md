# Customer Segmentation & Profiling Project

### Objective
Segment online retail customers based on purchasing behavior using RFM (Recency, Frequency, Monetary) analysis and K-Means clustering to uncover actionable insights for marketing and customer relationship management.

---

## Dataset
- **Source:** Kaggle — UK-based E-Commerce Dataset (2010–2011)
- **Size:** 540,000 transactions
- **Key Columns:** InvoiceNo, StockCode, Description, Quantity, UnitPrice, CustomerID, InvoiceDate, Country

---

## Methodology
1. **Data Understanding** – Examined dataset structure and summary statistics.
2. **Data Cleaning & Preparation** – Removed cancelled invoices, negative/zero quantities, and missing CustomerIDs.
3. **RFM Feature Engineering** – Calculated:
   - Recency (days since last purchase)
   - Frequency (number of unique invoices)
   - Monetary (total spending)
4. **Data Preprocessing for Clustering** – Applied log transformation and standard scaling to normalize features.
5. **K-Means Clustering** – Determined optimal clusters (k=3) using Elbow and Silhouette methods.
6. **Cluster Analysis & Interpretation** – Interpreted behavioral profiles using RFM averages.
7. **Visualization** – Created heatmaps and barplots to illustrate cluster characteristics.

---

## Results 

| Cluster | Recency | Frequency | Monetary | Segment Description |
|----------|----------|------------|-----------|----------------------|
| 0 | 31.16 | 9.69 | 4913.36 | Loyal, high-value customers — frequent, high spenders |
| 1 | 54.94 | 2.04 | 575.19 | Inactive, low-value customers — disengaged or churned 
| 2 | 253.69 | 1.39 | 370.11 |Mid-tier customers — moderate engagement and potential growth |

---

## Model Evaluation
- **Elbow Method:** Confirmed point of diminishing returns in inertia.
- **Silhouette Score:** Achieved best separation at k=3.
- **Qualitative Validation:** Clusters were distinct, interpretable, and aligned with business logic.

---

## Insights & Recommendations
- **Cluster 0:** Maintain loyalty through personalized rewards and VIP perks.
- **Cluster 1:** Limited-time discounts and targeted re-engagement, and encourage upselling
- **Cluster 2:** Personalized offers and gamified rewards, and customer retention by awarding points for repeat purchases.

---

## Files Included
| File | Description |
|------|--------------|
| 'rfm_final_clusters.csv' | Final, polished dataset with CustomerID, RFM metrics, and cluster labels |
| 'ecommerce_data.csv' | original, unpolished dataset |
| 'cluster_heatmap.png' | RFM cluster heatmap showing average values |
| 'cluster_3d.png' | 3D scatterplot showing cluster separation |
| 'customer_segmentation.ipynb' | Main notebook with full workflow |

---

## Tools & Libraries
Python, pandas, numpy, matplotlib, seaborn, scikit-learn

---

## Conclusion
K-Means clustering successfully identified three behaviorally distinct customer groups based on RFM metrics. The analysis provided insights into customer loyalty, engagement, and spending patterns, enabling targeted marketing and improved customer retention strategies.
