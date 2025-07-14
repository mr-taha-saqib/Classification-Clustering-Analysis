# E-Commerce Product Return Prediction & Business Traveler Segmentation

This repository contains two machine learning tasks: a **Classification Task** to predict product returns in e-commerce, and a **Clustering Task** to segment business travelers based on travel behavior and budget.

---

## 📌 Part I: Classification Task – Predicting Product Returns

### 🧠 Objective
Develop a predictive model that determines whether a product will be returned by a customer, helping e-commerce platforms reduce logistical costs and enhance customer satisfaction.

### 📊 Dataset
- Contains 14 independent numerical features.
- Target variable: `returned` (1 = returned, 0 = not returned).

### 🔍 Features Grouped by Category
- **Customer Behavior**: `customer_satisfaction`, `time_on_product_page`, `return_history_count`, etc.
- **Product Characteristics**: `discount_percentage`, `product_price`, `product_weight_kg`, etc.
- **Logistics Factors**: `delivery_delay_days`, `warehouse_distance_km`, `days_to_shipment`

### 🛠️ Models Used
- **Logistic Regression**
- **K-Nearest Neighbors (KNN)** with Grid Search

### ⚙️ Preprocessing
- Standardization using Z-score normalization
- Stratified Train/Test Split (80/20)
- 5-fold Cross-Validation

### 📈 Evaluation Metrics
- Accuracy
- Precision, Recall, F1 Score
- ROC-AUC Score
- ROC Curve Visualization

### ✅ Model Recommendation
**Logistic Regression** was recommended for deployment due to its:
- High and balanced performance
- Higher AUC score (0.966)
- Interpretability for business decisions

---

## 📌 Part II: Clustering Task – Business Traveler Segmentation

### 🧠 Objective
Use unsupervised learning to segment business travelers based on:
- `yearly_trips`
- `budget`

### 📊 Dataset
- 1000 records with behavioral and financial attributes of business travelers.

### 🛠️ Techniques Used
- **K-Means Clustering** (k=3)
- **Agglomerative Hierarchical Clustering** (dendrogram + linkage matrix)
- **Principal Component Analysis (PCA)** for dimensionality reduction and visualization

### 📉 PCA
- PCA reduced dimensionality while preserving data variance.
- Clusters were re-evaluated in PCA space.

### 📈 Visualizations
- Scatterplots of clustering results (original and PCA space)
- Dendrogram for hierarchical clustering
- ROC Curves for classification models

### 🧩 Clustering Insights
Identified 3 main traveler segments:
1. **Frequent Business Travelers**
2. **Occasional Budget Travelers**
3. **Luxury-Oriented Travelers**

### ✅ Preferred Clustering Method
**Agglomerative Hierarchical Clustering** was preferred due to:
- Stable cluster formation
- Rich insights via dendrogram
- Better interpretation of nested relationships

---
