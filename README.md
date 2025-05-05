# 🧠 Stroke Data Analysis and Visualization

This project presents a full data analysis pipeline on the **Healthcare Stroke Dataset**. It includes data preprocessing, visualization, dimensionality reduction (PCA, UMAP, t-SNE), and clustering (KMeans, DBSCAN). The goal is to explore patterns that may be associated with stroke occurrence.

## 📊 Dataset Description

The dataset contains medical and demographic data about patients, with the target variable being whether the patient had a stroke (`stroke`: 0 or 1).

## 🧼 Data Preprocessing

- Filled missing `bmi` values using **median** imputation
- Dropped rows with gender "Other"
- Kept "Unknown" as a valid category in `smoking_status`
- One-hot encoded categorical features
- Scaled features using `StandardScaler`

## 📉 Dimensionality Reduction

Used 3 methods to visualize and reduce data into 2D:

- **PCA (Principal Component Analysis)**
- **UMAP (Uniform Manifold Approximation and Projection)**
- **t-SNE (t-distributed Stochastic Neighbor Embedding)**

## 🔍 Clustering

Tried to find structure using unsupervised clustering:

- **KMeans**: Performed poorly on this unbalanced dataset
- **DBSCAN**: Slight improvement, discovered a small cluster of stroke patients
- **ARI (Adjusted Rand Index)** used to evaluate clustering quality


🧠 Key Takeaways
The dataset is highly imbalanced: ~5% of patients had a stroke.
Unsupervised learning methods (like clustering) are not sufficient to detect stroke risk.
For real prediction tasks, supervised classification models are more suitable (e.g., logistic regression, random forest, etc.)

🛠️ Technologies Used
Python (Pandas, NumPy, Matplotlib, Seaborn)
Scikit-learn
UMAP
t-SNE
Jupyter Notebook

📜 License
This project is open-source under the MIT License.
