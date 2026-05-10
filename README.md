# Automatic Grouping of Dry Beans Using Unsupervised Learning

This project applies unsupervised learning methods to the Dry Bean Dataset. The main goal is to group dry bean samples based on their physical features without using the class labels during clustering.

---

## Project Overview

A large volume of dry beans may need to be sorted regularly. This project explores whether unsupervised machine learning can support this process by grouping beans according to physical and shape-related measurements.

The project includes:

- data loading and inspection
- exploratory data analysis
- preprocessing and outlier removal
- feature scaling
- dimensionality reduction with PCA
- clustering with K-Means, DBSCAN, and Hierarchical Agglomerative Clustering (HAC)
- clustering evaluation using Silhouette Score and Davies-Bouldin Index

---

## Dataset

The dataset used in this project is the Dry Bean Dataset from the UCI Machine Learning Repository.

Source:  
https://archive.ics.uci.edu/dataset/602/dry+bean+dataset

The dataset contains 13,611 dry bean samples and 16 numerical features. These features describe physical and shape-related properties such as area, perimeter, axis length, roundness, compactness, and shape factors.

The original dataset also includes a `Class` column with seven bean types. This label column was removed before clustering because the project follows an unsupervised learning approach.

### Authors

- Assoc. Prof. Dr. Murat Köklü
- Assoc. Prof. Dr. İlker Ali Özkan


### License

Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Methods

The following methods are used in the project:

### Preprocessing
- IQR-based outlier removal
- StandardScaler for feature scaling

### Dimensionality Reduction
- Principal Component Analysis (PCA)

### Clustering Algorithms
- K-Means
- DBSCAN
- Hierarchical Agglomerative Clustering (HAC)

### Evaluation Metrics
- Silhouette Score
- Davies-Bouldin Index

---

## Main Result

The final selected clustering result is K-Means on the PCA-transformed dataset with `k = 2`.

Final evaluation results:

- Silhouette Score: `0.465`
- Davies-Bouldin Index: `0.878`

The clustering quality is moderate. The final clusters mainly separate beans according to size and shape morphology.

---

## Files

- `01_full_experimental_analysis.ipynb` → exploratory clustering analysis with K-Means, DBSCAN, and HAC
- `02_final_clustering_analysis.ipynb` → final clustering analysis and conclusions
- `Dry_Bean_Dataset.xlsx` → dataset file

---

## Requirements

Main Python libraries used in the project:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy
- plotly
- openpyxl

---

## Notes

- The project follows a fully unsupervised learning approach.
- PCA reduced the dataset from 16 dimensions to 3 while preserving 89.62% of the variance.
- The clustering structure was moderate rather than strongly separated.
