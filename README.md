# MSc_Data_Science_Project
# Customer Segmentation using Clustering Techniques

## Project Overview
This project focuses on customer segmentation using unsupervised machine learning techniques applied to transactional retail data. The objective is to identify meaningful customer groups based on purchasing behaviour to support targeted marketing and business decision-making.

The analysis is performed using the Online Retail dataset and follows a complete data science workflow including data preprocessing, exploratory data analysis, feature engineering, clustering, and model evaluation.

---

## Objectives
- Transform transaction-level data into customer-level insights using RFM (Recency, Frequency, Monetary) analysis
- Apply clustering algorithms to segment customers
- Compare multiple clustering techniques
- Evaluate model performance using internal clustering metrics
- Improve clustering performance using dimensionality reduction

---

## Dataset
- **Name:** Online Retail Dataset  
- **Source:** UCI Machine Learning Repository  
- **Link:** https://archive.ics.uci.edu/ml/datasets/Online+Retail  
- **Format:** Excel (.xlsx)  
- **Size:** 541,909 records and 8 features  
- **Period Covered:** December 2010 – December 2011  

---

## Methodology

### 1. Data Preprocessing
- Removed missing CustomerID values
- Filtered out cancelled transactions
- Removed invalid quantity and unit price values
- Removed duplicate records
- Created TotalPrice feature

### 2. Exploratory Data Analysis (EDA)
- Analyzed transaction distribution across countries
- Examined revenue trends over time
- Investigated distributions of quantity and unit price
- Identified skewness and outliers

### 3. Feature Engineering
- Converted transaction data into customer-level RFM features:
  - Recency: Days since last purchase
  - Frequency: Number of transactions
  - Monetary: Total spend

### 4. Data Transformation
- Applied log transformation to reduce skewness
- Standardized features using StandardScaler

---

## Models Implemented
- K-Means Clustering
- Hierarchical Clustering (Agglomerative)
- DBSCAN

---

## Model Evaluation Metrics
- Silhouette Score
- Davies–Bouldin Index
- Calinski–Harabasz Score

---

## Results

| Model         | Silhouette Score |
|--------------|------------------|
| K-Means      | 0.416            |
| Hierarchical | 0.401            |
| DBSCAN       | 0.333            |

---

## Performance Improvements

### Outlier Removal
- Applied IQR method
- Result: Slight decrease in performance

### Dimensionality Reduction (PCA)
- Applied PCA before clustering
- Improved silhouette score from **0.416 to 0.463**

---

## Final Model
**PCA + K-Means Clustering**

This combination provided the best cluster separation and interpretability.

---

## Customer Segments Identified

1. **High Value Loyal Customers**
   - High frequency and spending
   - Recent purchases

2. **Regular Customers**
   - Moderate purchasing behaviour
   - Potential for growth

3. **At Risk Customers**
   - Low engagement
   - Long time since last purchase

---

## Business Recommendations
- Loyalty programs for high-value customers
- Targeted promotions for regular customers
- Re-engagement strategies for at-risk customers

---

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

---

## Project Structure

├── DS_Project_Chirag.ipynb
├── README.md
├── MSc Data Science Project Report Chirag
└── online+retail.zip


---

## Reproducibility
To reproduce the results:
1. Download the dataset from the provided link
2. Open the Jupyter Notebook
3. Run all cells sequentially
4. Ensure required Python libraries are installed

---

## Conclusion
This project demonstrates how unsupervised learning techniques can be effectively applied to customer segmentation. The final model (PCA + K-Means) successfully identified meaningful customer groups that can support business decision-making.

---

## Author
Chirag  
MSc Data Science Student  
University of Hertfordshire

---

## License
This project is for academic purposes only.
