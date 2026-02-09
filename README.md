# ramyars-ml-task2
# K-Means Customer Segmentation – Prodigy InfoTech Task 2

## Overview

This project implements a K-Means clustering model to segment customers of a retail mall based on their purchasing behavior. [web:2][web:40]  
The goal is to identify meaningful customer groups so that the business can design targeted marketing strategies for each segment. [web:40][web:47]  

---

## Dataset

- **Name:** Mall Customer Segmentation Data  
- **Source:** Kaggle – "Mall Customer Segmentation Data" dataset. [web:2]  
- **Rows:** 200 customers. [web:2]  
- **Main features used:**
  - CustomerID
  - Gender
  - Age
  - Annual Income (k$)
  - Spending Score (1–100) – score assigned by the mall based on customer behavior and spending nature. [web:2]  

The clustering model in this project primarily uses **Annual Income (k$)** and **Spending Score (1–100)** as features. [web:2][web:44]  

---

## Objectives

1. Load and explore the mall customer dataset, checking distributions and relationships between variables. [web:40][web:44]  
2. Apply feature scaling and use K-Means clustering to group customers into meaningful segments. [web:40][web:47]  
3. Determine an appropriate number of clusters using the Elbow method and Silhouette score. [web:40][web:47]  
4. Visualize the resulting clusters and centroids, and interpret each segment from a business perspective. [web:39][web:44]  

---

## Project Structure

- `task2.ipynb` – Jupyter/Colab notebook containing all code, EDA, clustering steps, and visualizations.  
- `Mall_Customers_with_clusters.csv` – final dataset with all 200 customers and their assigned cluster labels.  
- `customer_segments.png` – scatter plot of Annual Income vs Spending Score colored by cluster, with centroids marked. [web:44]  
- `README.md` – project description and documentation.  

---

## Methodology

1. **Exploratory Data Analysis (EDA)**  
   - Checked for missing values and basic statistics of Age, Annual Income, and Spending Score. [web:40][web:42]  
   - Visualized feature distributions and the relationship between Annual Income and Spending Score. [web:40][web:44]  

2. **Feature Selection and Scaling**  
   - Selected `Annual Income (k$)` and `Spending Score (1-100)` as primary features for clustering. [web:2][web:44]  
   - Standardized features using `StandardScaler` to give them equal importance in distance calculations. [web:40][web:47]  

3. **Choosing the Number of Clusters (k)**  
   - Computed the within-cluster sum of squared errors (inertia) for k from 1 to 10 and plotted the Elbow curve. [web:40][web:44]  
   - Calculated Silhouette scores for k from 2 to 10 to evaluate cluster separation. [web:40][web:47]  
   - Both methods indicated that **k = 5** provides a good balance between compactness and separation of clusters. [web:40][web:46]  

4. **Model Training**  
   - Trained a K-Means model with 5 clusters on the scaled feature matrix. [web:40][web:47]  
   - Added the resulting cluster labels as a new `Cluster` column to the original dataset. [web:40][web:47]  

5. **Visualization and Interpretation**  
   - Plotted the clusters in the income–spending space and marked their centroids. [web:39][web:44]  
   - Computed mean Age, Annual Income, and Spending Score for each cluster to profile customer segments. [web:40][web:42]  

---

## Results

The model discovered **five distinct customer segments** based on income and spending behavior. [web:40][web:42]  
Below is an interpretation of each cluster (values approximate and based on the computed cluster means in the notebook):

1. **Cluster 1 – Premium / Loyal Customers**  
   - High annual income and high spending scores, mostly younger adults. [web:40][web:42]  
   - Represents highly valuable customers who frequently purchase and respond well to loyalty programs and premium offers. [web:40][web:47]  

2. **Cluster 2 – Young Trend Seekers**  
   - Low to medium income but high spending scores, generally younger customers. [web:42][web:44]  
   - Likely to respond to discounts, new product launches, and seasonal campaigns. [web:40][web:47]  

3. **Cluster 3 – Potential High-Value Customers**  
   - High income but low spending scores, often middle-aged customers. [web:42][web:46]  
   - Have strong purchasing power but currently under-utilized; can be targeted with personalized promotions to increase spending. [web:40][web:47]  

4. **Cluster 4 – Budget-Conscious Customers**  
   - Low income and low spending scores, typically older customers. [web:42][web:46]  
   - Prefer essential items and value-for-money products; respond to price-sensitive offers and bundles. [web:40][web:42]  

5. **Cluster 0 – Mainstream / Average Customers**  
   - Medium income and medium spending scores, covering a broad age range. [web:42][web:44]  
   - Represent the core customer base and are suitable for general-purpose marketing campaigns. [web:40][web:47]  

The final CSV file `Mall_Customers_with_clusters.csv` contains each of the 200 customers along with the corresponding cluster label (0–4). [web:40][web:47]  

---

## How to Run

1. Open the `task2.ipynb` notebook in Jupyter or Google Colab.  
2. Ensure `Mall_Customers.csv` is available in the working directory or uploaded to Colab. [web:2]  
3. Run all cells sequentially to reproduce EDA, clustering, plots, and the final CSV with cluster labels. [web:40][web:47]  

---

## Business Applications

- Design **targeted marketing campaigns** for each segment instead of one-size-fits-all promotions. [web:39][web:47]  
- Allocate budgets efficiently by investing more in premium and potential high-value customers. [web:38][web:42]  
- Develop personalized offers, loyalty programs, and pricing strategies aligned with the behavior of each segment. [web:39][web:47]  

---

## Technologies Used

- Python, NumPy, Pandas, Matplotlib, Seaborn. [web:40][web:47]  
- Scikit-learn for scaling, K-Means clustering, and evaluation metrics. [web:40][web:47]  
- Jupyter Notebook / Google Colab for experimentation and visualization. [web:40]  

---

## References

- Kaggle – Mall Customer Segmentation Data. [web:2]  
- Articles and tutorials on K-Means customer segmentation and mall customer analysis. [web:39][web:40][web:42][web:44][web:47]  
