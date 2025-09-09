# 🛍️ Customer Segmentation using K-Means

This project applies **K-Means Clustering** to segment mall customers based on their **Annual Income** and **Spending Score**.  
The goal is to identify distinct customer groups to support **targeted marketing strategies**.

---

## 📂 Dataset
- **Name**: Mall Customer Segmentation Data  
- **Source**: Kaggle ([Mall_Customers.csv](https://www.kaggle.com/vjchoudhary7/customer-segmentation-tutorial-in-python))  
- **Features**:
  - `CustomerID` → Unique customer ID  
  - `Gender` → Male/Female  
  - `Age` → Age of customer  
  - `Annual Income (k$)` → Income in thousands  
  - `Spending Score (1–100)` → Store-assigned score for spending behavior  

---

## ⚙️ Steps in the Project

### 1. Load Libraries
- `tidyverse` for data wrangling & visualization  
- `cluster` for clustering algorithms  
- `factoextra` for cluster visualization  

### 2. Data Preparation
- Select only **Annual Income** & **Spending Score**  
- Standardize features (`scale()`) to remove unit differences  

### 3. Determine Optimal Clusters
- I UseD **Elbow Method (WSS)**  
- fom the plot i decided to Choose `k = 5` as optimal  

### 4. Run K-Means
set.seed(123) (reproducibility)
km <- kmeans(df_scaled, centers = 5, nstart = 25)

### 5. Visualize Clusters
fviz_cluster() was used to plot clusters in 2D
Ellipses show cluster spread and separation

### 6. Interpret Results

Cluster 1: Average income, moderate spending
Cluster 2: Low income, low spending
Cluster 3: High income, high spending (potential premium customers 💎)
Cluster 4: High income, low spending (savers)
Cluster 5: Low income, high spending (value shoppers)

### 📊 Outputs

Elbow Method Plot → shows optimal cluster number
Cluster Plot → visualizes customer groups
Cluster Summary Table → avg income & spending per cluster
Bar Charts → compare average income & spending by cluster

### 🚀 How to Run

Clone this repo or download the .Rmd notebook.
Place Mall_Customers.csv in your working directory.
Open Customer-Segmentation-in-R.Rmd in RStudio.
Knit to HTML/Word/PDF for a full report.

🖊️ Author

Olusanya Joshua
Portfolio Project in R (Data Science)

### View Report 
[See the HTML report here](https://jhaybot.github.io/Customer-Segregation-R/)
