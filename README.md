# 🛍️ Mall Customer Segmentation using Machine Learning

A Machine Learning project that segments mall customers into different groups based on their **Annual Income** and **Spending Score** using the **K-Means Clustering** algorithm. The project helps businesses understand customer behavior and create targeted marketing strategies.

---

## 🚀 Features

- Customer data preprocessing and cleaning
- Exploratory Data Analysis (EDA)
- Optimal cluster selection using the Elbow Method
- Customer segmentation using K-Means Clustering
- Data visualization with scatter plots
- Export segmented customer data with cluster labels

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 📂 Project Structure

```
Mall-customer-Segmentation/
│
├── data/
│   └── Mall_Customers.csv
│
├── notebooks/
│   └── Mall_Customer_Segmentation.ipynb
│
├── images/
│   └── Cluster_Visualization.png
│
├── output/
│   └── Segmented_Customers.csv
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## 📊 Project Workflow

1. Load the customer dataset
2. Perform data cleaning and preprocessing
3. Explore customer demographics and spending behavior
4. Determine the optimal number of clusters using the Elbow Method
5. Train the K-Means clustering model
6. Assign cluster labels to customers
7. Visualize customer segments
8. Export the segmented dataset

---

## 📈 Dataset Features

The dataset includes:

- Customer ID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1–100)

The model primarily uses:

- Annual Income
- Spending Score

---

## 🤖 Machine Learning Model

**Algorithm Used:**

- K-Means Clustering (Unsupervised Learning)

### Model Highlights

- Optimal number of clusters selected using the Elbow Method
- Segmented customers into **5 meaningful groups**
- Generated cluster labels for each customer

---

## 📉 Sample Customer Segments

Examples of customer groups identified:

- High Income – High Spending
- High Income – Low Spending
- Low Income – High Spending
- Low Income – Low Spending
- Average Income – Average Spending

These insights can help businesses personalize marketing campaigns and improve customer engagement.

---

## 📊 Visualizations

The project generates:

- Elbow Method Graph
- Customer Cluster Scatter Plot
- Cluster Centroids Visualization

Example:

```
Cluster 1 ●
Cluster 2 ●
Cluster 3 ●
Cluster 4 ●
Cluster 5 ●
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/rohanb2005/Mall-customer-Segmentation.git
```

Navigate to the project folder:

```bash
cd Mall-customer-Segmentation
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open and run:

```
Mall_Customer_Segmentation.ipynb
```

---

## 📦 Required Libraries

```text
numpy
pandas
matplotlib
seaborn
scikit-learn
jupyter
```

---

## 📊 Output

The project generates:

- Customer cluster labels
- Cluster visualization graphs
- Segmented customer CSV file

---

## 🎯 Applications

- Customer Behavior Analysis
- Targeted Marketing
- Customer Retention Strategies
- Product Recommendation
- Business Intelligence
- Market Segmentation

---

## 🔮 Future Improvements

- Use DBSCAN and Hierarchical Clustering for comparison
- Build an interactive dashboard with Streamlit
- Add 3D cluster visualization
- Perform customer lifetime value analysis
- Deploy the project as a web application

---

## 👨‍💻 Author

**Rohan Bhavsar**

GitHub: https://github.com/rohanb2005

LinkedIn: *(Add your LinkedIn profile link here)*

---

## ⭐ Support

If you found this project useful, please give it a ⭐ on GitHub!

---

## 📄 License

This project is licensed under the MIT License.
