Purpose of Lab Work
This lab explores two unsupervised machine learning algorithms—K-Means Clustering and K-Medoids Clustering—applied to the Wine Dataset from sklearn. The goal is to understand clustering techniques, compare their effectiveness, and visualize cluster structures using evaluation metrics like the Silhouette Score and Adjusted Rand Index (ARI).

By applying and analyzing both algorithms, this lab demonstrates the differences between centroid-based and medoid-based clustering methods in terms of cluster formation, interpretability, and alignment with actual class labels.

 Steps Taken & Code Implementation
1. Library Setup & Environment Preparation:
Automated dependency checks and installations for:

scikit-learn, scikit-learn-extra, pandas, matplotlib.

Ensured reproducible environment with version verification.

2.  Data Loading & Preparation:
Loaded Wine Dataset using sklearn.datasets.load_wine().

Conducted exploratory data analysis:

Feature names and class distributions reviewed.

Standardized features using z-score normalization via StandardScaler() for distance-based clustering.

3.  K-Means Clustering:
Implemented using KMeans(n_clusters=3) (3 clusters for 3 wine classes).

Generated cluster labels and computed:

Silhouette Score (cluster compactness).

Adjusted Rand Index (ARI) (agreement with actual labels).

4.  K-Medoids Clustering:
Implemented using KMedoids(n_clusters=3) from scikit-learn-extra.

Generated cluster labels and computed:

Silhouette Score.

ARI.

5.  Visualization:
Used PCA (Principal Component Analysis) to project 13-dimensional data into 2D.

Created side-by-side scatter plots for:

K-Means (with centroids).

K-Medoids (with medoids).

Clearly marked centroids and medoids using large red ‘X’ markers for visual clarity.

6. Performance Comparison:
Tabulated and printed Silhouette Score and ARI for both algorithms.

Explained visual and metric-based differences between K-Means and K-Medoids.

7. Results Summary
| Algorithm     | Silhouette Score | Adjusted Rand Index (ARI) |
| ------------- | ---------------- | ------------------------- |
| **K-Means**   | 0.2849           | 0.8975                    |
| **K-Medoids** | 0.2660           | 0.7263                    |


K-Means achieved higher scores in both metrics, indicating better-defined clusters and stronger agreement with actual class labels.

K-Medoids handled non-spherical shapes more effectively but was less accurate on this dataset.

Visualizations
Clear PCA-based 2D scatter plots were created.

Clusters are easily distinguishable.

Centroids and medoids clearly marked.

Plots effectively communicate clustering patterns and performance differences.

 Observations & Recommendations
Cluster Quality:
K-Means formed slightly tighter clusters as shown by a higher Silhouette Score.

Clustering Agreement:
K-Means demonstrated better alignment with true class labels (higher ARI).

Cluster Shape Handling:
K-Medoids can manage non-spherical clusters and is less sensitive to outliers, but in this case, K-Means outperformed due to the data structure.

When to Prefer Each:

K-Means: Suitable when spherical clusters are expected and computational efficiency is important.

K-Medoids: Better for datasets containing noise or non-spherical clusters.

 Challenges Faced
Properly scaling features was critical to meaningful clustering.

Visualizing 13-dimensional data in 2D required careful PCA implementation.

Handling of outliers and sensitivity in K-Medoids necessitated understanding its behavior compared to K-Means.

 Repository Structure
MSCS_634_Lab_3.ipynb: Complete notebook with code, visualizations, and analysis.

README.md: This project summary and analytical explanation.

 Conclusion
This lab provided valuable insights into:

Distance-based clustering techniques.

The role of centroids vs. medoids in clustering.

Visualizing and comparing clustering outcomes.

Evaluating cluster quality using Silhouette Score and ARI.

Overall, K-Means proved more effective for this dataset, while K-Medoids remains useful for specialized clustering problems.
