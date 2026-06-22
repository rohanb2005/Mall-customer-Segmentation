# Mall-customer-Segmentation
Customer segmentation is the process of dividing customers into groups based on shared characteristics. In a mall context, this means grouping shoppers based on their spending habits and income so the business can target each group differently — for example, sending premium offers to high spenders and discount coupons to budget shoppers.

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("MallData.csv")
print("File imported Successfully")

df.shape
df.describe
df.info()

df.head()
df.isnull().sum()

df.columns

# StandardScaler : Tool used to scale data so all features are on same range.
from sklearn.preprocessing import LabelEncoder, StandardScaler
from sklearn.cluster import KMeans

#LabelEncoder() : converts text data into number
#fit() : learns the data patteerns 
#transform() : convert data to standard scale
le = LabelEncoder()
df['Gender'] = le.fit_transform(df['Gender'])
print("Done")

# StandardScaler() : Creates scaler object
scaler = StandardScaler()
scaled_data = scaler.fit_transform(df)

wcss = []
for i in range(1,11):
    kmeans = KMeans(n_clusters=i, random_state=42)
    kmeans.fit(scaled_data)
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11), wcss)
plt.xlabel("Number of Clusters")
plt.ylabel("WCSS")
plt.show()

# KMeans() → Creates KMeans clustering model.
kmeans = KMeans(n_clusters=5, random_state=42)
clusters = kmeans.fit_predict(scaled_data)

#df['Cluster'] : Creates a new column named Cluster
df['Cluster'] = clusters
df.head(20)
df.info()

plt.figure(figsize=(10,6))
sns.scatterplot(x='Annual Income',
                y='Spending Score',
                hue='Cluster',
                palette='Set2',
                data=df,
                s=100)
plt.title("Customer Segments")
plt.show()

df['Cluster'].value_counts()

df.to_csv('Mall_Customers_GMM_Segmented.csv', index=False)
print("Results saved! Ready for business use.")
