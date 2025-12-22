# Cluster Analysis of Utility Companies
This project is an end-to-end exploration of how unsupervised machine learning—specifically **Hierarchical** and **K-Means Clustering**—can transform raw operational metrics into a strategic roadmap for the energy sector. By segmenting utility companies based on financial and operational signatures, I’ve identified distinct profiles that help benchmark performance and identify market outliers.

## My Analytical Approach
To ensure the clusters were meaningful and statistically sound, I followed a structured data science workflow:
* **Normalization:** I applied Z-score standardization to the dataset. This was a critical step to ensure that high-magnitude variables (like `Sales`) didn't overshadow smaller but equally important metrics (like `Fuel_Cost`).
* **Hierarchical Clustering:** I used dendrograms to visualize the "family tree" of these utilities. By testing different linkage methods (Single and Complete), I determined how individual companies branched off based on Euclidean distance.
* **K-Means Optimization:** To find the "natural" number of groupings, I employed the Elbow Method. This led me to select **k=6** as the optimal number of clusters to balance detail with generalizability.

---

## Visual Interpretation: Clustermap & Centroids
I used two primary visualizations to interpret the model’s findings:

### 1. The Clustermap (Heatmap)

![Clustermap](Clustermap.png)

The heatmap provides a high-level view of how features drive the groupings. 
* **Feature Dominance:** I observed that the `Nuclear` column acts as a primary separator; companies with high nuclear reliance form a distinct vertical "band."
* **Cost vs. Growth:** Darker regions in `Demand_growth` and `Fuel_Cost` (seen in Cluster 1) immediately highlight utilities operating in high-growth, high-expense environments.

### 2. Parallel Coordinates (Cluster Centroids)

![Cluster Chart](clusterchart.png)

This chart displays the "average DNA" of each cluster across all normalized metrics.
* **Efficiency Leaders (Cluster 4):** This group is my "efficiency benchmark"—it maintains the highest `Sales` while keeping `Cost` and `Fuel_Cost` near the bottom of the scale.
* **Growth Outliers (Cluster 1):** This group shows a massive spike in `Demand_growth` but is distinctively low in `Nuclear` energy, suggesting a reliance on traditional or renewable expansion.

---

## Segmentation Summary
| Cluster Group | Size | Performance Profile | Key Member Examples |
| :--- | :---: | :--- | :--- |
| **Cluster 0** | 5 | Stable, moderate operational metrics. | Industry "Standard" |
| **Cluster 1** | 1 | **High Growth Outlier:** Extreme demand with no nuclear. | Nevada, Idaho |
| **Cluster 2** | 6 | Major group with consistent financial signatures. | Large-scale Utilities |
| **Cluster 3** | 3 | Niche group with tight operational alignment. | San Diego |
| **Cluster 4** | 1 | **Sales Leader:** High revenue with low fuel overhead. | Efficiency Model |
| **Cluster 5** | 6 | **Nuclear Dependent:** High reliance on nuclear power. | Energy-Heavy |

---

## Strategic Impact & Business Findings
Through this analysis, I’ve identified three key areas where these findings provide actionable value:
- **Infrastructure Strategy:** Utilities in high-growth clusters (Cluster 1) require aggressive capital investment forecasting compared to the stable "Standard" groups.
- **Operational Benchmarking:** Companies in the high-cost clusters can look toward the signatures of **Cluster 4** as a target for optimizing their fuel-to-sales ratios.
- **Risk Profiling:** By identifying outliers like San Diego or Nevada, stakeholders can recognize unique market risks—such as specialized regulatory environments or geographic constraints—that don't fit the industry average.

## Technologies Used
* **Python** (Pandas, NumPy)
* **Scikit-Learn:** K-Means and Z-score Scaling
* **SciPy:** Hierarchical Clustering & Dendrograms
* **Visualization:** Matplotlib & Seaborn

---

## 🚀 How to Run This Project
To replicate the cluster analysis on your local machine, follow these steps:

### 1. Clone the Repository
```bash
git clone [https://github.com/NnekaE/Clustering_Utilities-.git](https://github.com/NnekaE/Clustering_Utilities-.git)
cd Clustering_Utilities-

pip install pandas scikit-learn scipy matplotlib seaborn
 
jupyter notebook Clustering_Utilities.ipynb
