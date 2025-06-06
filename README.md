# Task 8: Clustering with K-Means - Mall Customer Segmentation

## 📌 Objective (AIM)

The goal of this task is to perform **unsupervised learning** using the **K-Means Clustering** algorithm on the **Mall Customer Segmentation dataset**. This helps us understand different groups of customers based on their behavior like income and spending score.

---

## Dataset Used

**Mall_Customers.csv**  
Path: `data/Mall_Customers.csv`

This dataset includes the following columns:
- `CustomerID`
- `Gender`
- `Age`
- `Annual Income (k$)`
- `Spending Score (1-100)`

---

## 🧪 Tools and Libraries Used

- **Pandas**: For data manipulation and loading
- **Matplotlib & Seaborn**: For visualization
- **Scikit-learn**: For clustering, preprocessing, and evaluation

---

## File Structure
project_folder/  
│  
├── data/  
│   └── Mall_customers.csv  
│  
├── ml-task-kmeans-clustering.ipynb  
└── README.md  

---

## Step-by-Step Workflow

### Step 1: Load and Explore the Dataset
- Loaded the dataset using `pandas`.
- Displayed the first few rows to understand the data structure.

### Step 2: Data Preprocessing
- Checked for missing values.
- Encoded the `Gender` column using `LabelEncoder` (K-Means needs numerical data).
- Selected relevant features: **Annual Income** and **Spending Score**.

### Step 3: Visualize the Data
- Plotted a scatterplot of Income vs. Spending Score to get a visual sense of potential clusters.

### Step 4: Find the Optimal Number of Clusters (K)
- Used the **Elbow Method**:
  - Ran K-Means for K = 1 to 10.
  - Plotted **inertia** (within-cluster sum of squares) for each K.
  - The “elbow” point suggested **K = 5** as optimal.

### Step 5: Apply K-Means Clustering
- Applied KMeans with **K = 5**.
- Assigned predicted cluster labels to each data point.

### Step 6: Visualize the Clusters
- Used `seaborn` to plot clusters with different colors.
- Plotted centroids to show the center of each cluster.

### Step 7: Evaluate the Clustering
- Calculated the **Silhouette Score** to evaluate how well the clustering was performed.
- A higher score indicates better-defined clusters.

---

## Results

- **Optimal Number of Clusters (K):** 5 (via Elbow Method)
- **Silhouette Score:**  `0.554` – indicating fairly good separation between clusters.
- Created visual plots to show how customers group based on income and spending.

---

## Learnings

- K-Means is sensitive to feature scaling and initial centroids, but great for segmentation.
- The Elbow Method is a visual tool to choose the best number of clusters.
- Silhouette Score is useful for evaluating clustering quality.
- Data preprocessing and feature selection are crucial for meaningful clusters.

---
