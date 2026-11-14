## DSC8307 – Data Mining, Modeling and Analytics  
Advent 2026 Assignment

**Programme:** Master of Science in Data Science and Analytics  
**Course Code:** DSC8307  
## How to Run

1. Open the notebooks in Google Colab or Jupyter.
2. Place the datasets in `/content/`:
   - `wholesale-customers.csv`
   - `creditcard.csv`
3. Install dependencies:
   ```bash
   pip install -r requirements.txt


# Project 1 – Wholesale Customers

The dataset has 440 customers and their annual spending on six product categories. The data are heavily right-skewed, so a log transform and standardisation were applied. Channel and Region were dropped because the goal is segmentation by spending behaviour only. The Hopkins statistic (~0.80) confirmed the data are suitable for clustering.

K-Means, hierarchical clustering and DBSCAN were compared. K-Means and hierarchical clustering both gave clear, similar results with three clusters. DBSCAN mainly flagged outliers and was less useful for balanced segments. K-Means was preferred for interpretability.

The three segments are:  
- Fresh-focused Horeca customers (high Fresh/Frozen) – serve with volume discounts and frequent deliveries.  
- Retail/Convenience customers (high Milk, Grocery, Detergents) – serve with product bundles and reliable delivery.  
- High-volume diversified customers (high spend across most categories) – serve with dedicated account managers and priority logistics.
