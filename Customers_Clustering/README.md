# Machine Learning Clustering Project

This project demonstrates the application of clustering techniques on a customer dataset to group individuals into distinct clusters based on their features. The key steps include data preprocessing, applying KMeans clustering, using PCA for dimensionality reduction, and visualizing the results.

## Features
- **Data Preprocessing**: Cleaning, normalizing, and encoding the dataset.
- **KMeans Clustering**: Determining optimal clusters using Elbow Method and Silhouette Analysis.
- **Dimensionality Reduction**: Using PCA to reduce the dataset to 2 components for visualization.
- **Visualization**: Plotting clusters with consistent colors across training and test datasets.

## Dataset
The dataset contains the following columns:
- `CustomerID`: Unique identifier for each customer (removed during preprocessing).
- `Gender`: Gender of the customer (encoded as 1 for Female, 0 for others).
- `Age`: Age of the customer.
- `Annual Income (k$)`: Annual income in thousands of dollars.
- `Spending Score (1-100)`: Score assigned based on spending behavior.

## Workflow

### 1. Data Preprocessing
- Loaded the dataset using `pandas`.
- Split the data into training (80%) and testing (20%) sets.
- Removed irrelevant columns (`CustomerID`).
- Normalized numerical features (`Age`, `Annual Income`, `Spending Score`) using `StandardScaler`.
- Encoded the `Gender` column into binary values (Female = 1, others = 0).

### 2. Optimal Number of Clusters
- Used the Elbow Method to identify the point where inertia significantly decreases.
- Used Silhouette Analysis to measure cluster quality and determine the best number of clusters.
- Ran KMeans multiple times for each `k` to select the configuration with the least inertia.

### 3. Clustering
- Applied KMeans clustering to the training dataset.
- Predicted cluster labels for the test dataset.
- Saved test predictions to a CSV file (`predicts.csv`).

### 4. Dimensionality Reduction
- Reduced the dataset to 2 dimensions using PCA for better visualization.
- Ran KMeans again on the PCA-reduced training dataset.
- Predicted clusters for the PCA-reduced test dataset.
- Added PCA cluster predictions to the previously saved CSV file.

### 5. Visualization
- Visualized clusters for training and test datasets in PCA space.
- Used consistent colors for clusters across training and test datasets.
- Marked cluster centers with distinct symbols.

## Results
- Generated a `predicts.csv` file with the following columns:
  - Original features (`Gender`, `Age`, `Annual Income`, `Spending Score`).
  - Cluster predictions from original data.
  - Cluster predictions from PCA-reduced data.
- Visualized clusters to confirm well-separated groups.

![image](https://github.com/user-attachments/assets/0a1ab51d-d3b4-4a88-a701-7d2a44740685)


## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ml-clustering-project.git
   ```
2. Run the project in a Jupyter Notebook environment.

3. Modify the `your_file_path.csv` in the code to point to your dataset.

## Files
- `clustering_project.ipynb`: Contains all code for preprocessing, clustering, and visualization.
- `Mall_Customers.csv`: Dataset for this project.
- `predicts.csv`: Output file with cluster predictions.

## Dependencies
- Python 3.7+
- pandas
- scikit-learn
- matplotlib
- numpy

