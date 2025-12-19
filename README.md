 # Cluster Analysis of Utility Companies

This project performs a comprehensive cluster analysis on a utilities dataset to group companies based on their financial and operational performance metrics.  

## Project Overview ##

In this analysis, I explored how different utility companies naturally segment into groups using two primary clustering techniques: Hierarchical Clustering and K-Means.  

## Key Steps & Methodology ##

* Data Preparation: Loaded the utilities dataset and performed essential data cleaning.  
* Normalization: Applied Z-score standardization to ensure variables with different scales, such as Sales and Fuel Cost, contributed equally to the model.  
* Distance Metrics: Calculated Euclidean distances to measure the similarity between different company profiles.  
* Hierarchical Clustering: Used Dendrograms and various linkage methods (Single and Complete) to visualize the branching relationships between companies.  
* K-Means Clustering: Employed the Elbow Method to determine the optimal number of clusters (k) and segmented the utilities into distinct groups.

## Business Insights & Findings ##

Through this analysis, I identified several key business insights based on how the utility companies grouped together:  
* Efficiency Leaders: One cluster stood out with high sales and low fuel costs, representing the most operationally efficient companies in the dataset.  
* High-Cost Clusters: Another group was characterized by high fixed charges and lower rates of return, suggesting these companies may need to re-evaluate their infrastructure investments or pricing models.  
* Market Outliers: The analysis revealed specific companies that did not fit neatly into large clusters, highlighting unique market players with unconventional operational profiles.  

## Final Outcome ##
By the end of the project, I successfully segmented the utilities into distinct groups. This provides a clear framework for understanding market patterns and making data-driven business recommendations for each specific cluster.  

## Conclusion ##
This project demonstrates how unsupervised learning can transform raw operational data into actionable business intelligence. By identifying these clusters, utility managers can tailor their strategies—such as optimizing fuel costs for one specific group or adjusting rate structures for another—rather than applying a one-size-fits-all approach. This analysis serves as a foundation for more advanced predictive modeling or targeted resource allocation in the utilities sector.  

## Technologies Used ##
### Python  
* Pandas for data manipulation  
* Scikit-Learn for K-Means and scaling  
* SciPy for hierarchical clustering and dendrogram visualization  
* Matplotlib & Seaborn for data visualization  


