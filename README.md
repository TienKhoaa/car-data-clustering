# 🚗 Vehicle Data Analysis & K-Means Clustering

## 📌 Project Overview
This project focuses on extracting, cleaning, and clustering a dataset of used and new vehicles in Vietnam. The goal is to segment the car market based on key attributes such as mileage (`km`), price (`price`), and vehicle condition (`new_old`) using Unsupervised Machine Learning techniques.

By applying **K-Means Clustering**, the project successfully groups vehicles into distinct market segments, providing valuable insights into how vehicle depreciation and pricing behave across different usage levels.

## 🛠️ Tech Stack & Tools
- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib
- **Algorithms:** K-Means Clustering, DBSCAN, Principal Component Analysis (PCA)
- **Environment:** Jupyter Notebook / Google Colab

## 📊 Dataset Description
The dataset contains information about various cars available on the market. 
- **Raw size:** ~39,400 records.
- **Key Features Extracted for Modeling:**
  - `km`: Mileage of the vehicle.
  - `price`: Price of the vehicle (parsed from Vietnamese textual format like "Tỷ", "Triệu" into numerical floats).
  - `new_old`: Condition of the vehicle (Encoded as `0` for Old, `1` for New).

## 🧠 Methodology & Workflow
1. **Data Preprocessing & Cleaning:**
   - Parsed complex string values in the `price` column into standard numerical formats.
   - Cleaned the `km` string column by removing units and commas.
   - Handled missing values and mapped categorical variables (`Xe mới`/`Xe cũ` to `1`/`0`).
2. **Feature Scaling:**
   - Applied `StandardScaler` to normalize the data variance, preventing features with larger scales (like `price` and `km`) from dominating the distance calculations.
3. **Clustering Optimization:**
   - Utilized the **Elbow Method** (plotting Inertia) to identify the optimal number of clusters ($k=4$).
4. **Model Evaluation & Visualization:**
   - Evaluated the K-Means model using the **Silhouette Score**.
   - Applied **Principal Component Analysis (PCA)** to reduce dimensionality to 3 components for 3D scatter plot visualization.
   - Implemented an alternative density-based clustering algorithm (**DBSCAN**) for comparison.

## 📈 Key Results
- **Optimal Clusters:** Identified **4 distinct vehicle segments** in the market.
- **Silhouette Score:** Achieved an outstanding score of **~0.849**, indicating highly dense and well-separated clusters.
- **Business Insight:** The model visually proves a strong inverse correlation between mileage and price. It distinctly isolates "brand new high-price cars" from "high-mileage budget cars."

*(Optional: Add screenshots of your plots here)*

### 1. Elbow Method to Determine Optimal 'k'
> Add your Elbow Method plot image here (e.g., `![Elbow Plot](link_to_image)`)

### 2. K-Means Clustering Results (Price vs KM)
> Add your Scatter plot image here 

### 3. PCA 3D Visualization
> Add your 3D plot image here

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/car-data-clustering.git](https://github.com/your-username/car-data-clustering.git)# car-data-clustering
Data Analysis and K-Means Clustering on Vehicle Dataset.
1. Install the required dependencies:
pip install pandas numpy scikit-learn matplotlib
2. Open car_clustering_analysis.ipynb in Jupyter Notebook to explore the code.
