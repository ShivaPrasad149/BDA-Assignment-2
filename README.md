# BDA-Assignment-2

## Overview
This repository demonstrates both **supervised** and **unsupervised** machine learning approaches on the Iris dataset using PySpark. The aim is to classify iris flower species and group them into clusters using two different models:

- Logistic Regression (Classification)
- KMeans Clustering (Unsupervised Clustering)
- ALS Model (Collaborative Filtering Recommendation)

---

## Technologies Used
- Python 3
- Apache Spark (PySpark)
- Jupyter Notebook
- Pandas, Matplotlib

---

## Dataset
- **Iris Dataset**: [UCI Iris Dataset](https://raw.githubusercontent.com/uiuc-cse/data-fa14/gh-pages/data/iris.csv)
- **MovieLens Dataset**: [GroupLens - MovieLens](https://files.grouplens.org/datasets/movielens/ml-latest-small.zip)

---

## Model 1: Logistic Regression (Classification)

### Workflow:
1. Load and preview the Iris dataset.
2. Use `StringIndexer` to encode the `species` column as numerical labels.
3. Use `VectorAssembler` to combine feature columns.
4. Split the dataset into training and testing sets.
5. Train a `LogisticRegression` model using Spark MLlib.
6. Evaluate the model using test accuracy.
7. Predict species for new data points.
8. Convert numerical predictions back to species names.

### Highlight:
- Predicts the probability distribution of each class.
- Outputs accuracy and refined predictions.

---

## Model 2: KMeans Clustering (Unsupervised Learning)

### Workflow:
1. Load and assemble feature vectors.
2. Apply `KMeans` clustering with k=3.
3. Assign clusters to all records.
4. Evaluate clustering using silhouette score.
5. Print cluster centers.
6. Predict clusters for new data points.
7. Visualize clusters using Sepal and Petal features.

### Highlight:
- Shows natural grouping of flowers.
- Visualizations provided for cluster interpretation.

---

## Model 3: ALS (Collaborative Filtering Recommendation)

### Workflow:
1. Load the MovieLens ratings dataset.
2. Explore number of users, movies, and total ratings.
3. Preprocess the data by handling missing values.
4. Split the data into training and testing sets.
5. Build and train an ALS model.
6. Evaluate performance using RMSE.
7. Generate top-N recommendations for users and movies.
8. Display specific recommendations (e.g., for a user or a movie).
9. Analyze top users and insights.

### Highlight:
- Recommends movies to users and users to movies.
- Based on collaborative filtering using ALS.

---

## How to Run
1. Install PySpark and required libraries:
   ```bash
   pip install pyspark pandas matplotlib
   ```
2. Open the notebook file and run each cell sequentially.
3. Results including accuracy, clusters, recommendations, and visualizations will be displayed.

---

## Author
Developed as part of a Big Data Analytics assignment to demonstrate practical application of Spark MLlib for classification, clustering, and recommendation systems.

