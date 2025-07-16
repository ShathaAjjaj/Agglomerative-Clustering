# Wholesale Customers Clustering with Agglomerative Hierarchical Clustering

This project applies **Agglomerative Hierarchical Clustering** to segment customers in the **Wholesale Customers Dataset** based on their annual spending on different product categories. It includes data preprocessing, dendrogram visualization, clustering, and interpretation of the resulting customer segments.

## 📊 Dataset

The dataset contains annual spending (in monetary units) on the following product categories by different customers:

- Fresh
- Milk
- Grocery
- Frozen
- Detergents_Paper
- Delicatessen

Each row represents a customer.

Source: [UCI Machine Learning Repository - Wholesale Customers Data Set](https://archive.ics.uci.edu/ml/datasets/wholesale+customers)

## 🔍 Goal

To group customers into clusters based on their spending behavior and extract business insights that can be used for:

- Customer segmentation
- Targeted marketing
- Inventory optimization
- Sales strategy

## 🧪 Steps Performed

1. **Data Loading & Preprocessing**
   - Load dataset and select relevant features.
   - Scale features using `StandardScaler`.

2. **Dendrogram Plotting**
   - Use `scipy.cluster.hierarchy` to plot a dendrogram and visually choose the optimal number of clusters.

3. **Agglomerative Clustering**
   - Apply `AgglomerativeClustering` from `sklearn` with `ward` linkage.
   - Assign cluster labels to each customer.

4. **Visualization**
   - Scatter plot using `Milk` vs `Grocery` spending colored by cluster label.

5. **Cluster Profiling**
   - Calculate average spending per cluster to understand different customer types.

## 📈 Example Cluster Insights

| Cluster | Fresh      | Milk       | Grocery    | Frozen     | Detergents_Paper | Delicatessen | Interpretation                     |
|---------|------------|------------|------------|------------|------------------|--------------|------------------------------------|
| 0       | 11,802     | 5,010      | 6,973      | 2,784      | 2,383            | 1,371        | Balanced buyers                    |
| 1       | 22,015     | 9,937      | 7,844      | 47,939     | 672              | 4,154        | Frozen-focused businesses          |
| 2       | 15,965     | 34,709     | 48,537     | 3,055      | 24,875           | 2,943        | Grocery and Detergents heavy       |
| 3       | 36,847     | 43,950     | 20,170     | 36,534     | 239              | 47,943       | Very high spenders, diverse needs  |

## 🛠️ Technologies Used

- Python
- pandas
- matplotlib
- seaborn
- scikit-learn
- scipy

## Interpretation:

Cluster 0:
Moderate spending across most categories, with highest spending in Fresh and Grocery but relatively low on Milk and Delicatessen.
→ Possibly smaller restaurants or fresh food sellers focused on fresh produce.

Cluster 1:
Extremely high spending on Frozen (47,939) and Delicatessen (4,154), with moderate spending in Fresh and Grocery, but low in Detergents_Paper.
→ Likely businesses specializing in frozen goods — maybe catering services or frozen food retailers.

Cluster 2:
Very high spending on Milk (34,709), Grocery (48,537), and Detergents_Paper (24,875), but low on Frozen.
→ Probably supermarkets or convenience stores with a focus on dairy, grocery, and cleaning supplies.

Cluster 3:
Highest spending in Fresh (36,847), Milk (43,950), Frozen (36,534), and Delicatessen (47,943), but very low on Detergents_Paper.
→ Could be large wholesalers or big supermarkets with diverse product demands.


## What can you do with this?

Targeted marketing: Tailor campaigns to cluster needs — e.g., promote frozen products to Cluster 1, detergents and paper products to Cluster 2.

Sales strategy: Assign sales reps specialized by cluster product profiles.

Inventory management: Stock items in line with cluster purchasing behavior.

Customized offers: Create bundle offers fitting each cluster’s preferences.

## 🚀 How to Run
 Clone the repository:
   ```bash
   git clone https://github.com/ShathaAjjaj/wholesale-clustering.git
   cd wholesale-clustering

