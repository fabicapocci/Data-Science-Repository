# HR Candidate Segmentation with Clustering

## Overview

This project applies unsupervised machine learning techniques to identify meaningful candidate segments within an HR dataset.

Candidate characteristics are analyzed using K-Means and Agglomerative Clustering. The project explores cluster quality using the elbow method, silhouette scores, hierarchical clustering, and cluster profiling.

The existing job-change target is excluded from the clustering process and examined afterward to determine whether independently discovered candidate segments exhibit different job-change behavior.

## Project Workflow

1. Loaded and explored the HR candidate dataset
2. Removed identifier, index, and target variables from the clustering feature set
3. Standardized numerical features using StandardScaler
4. Applied K-Means clustering
5. Evaluated different numbers of clusters using inertia and silhouette scores
6. Profiled candidate characteristics within the resulting clusters
7. Examined job-change rates after clustering
8. Applied Agglomerative Clustering with Ward linkage
9. Visualized hierarchical structure using a dendrogram
10. Compared K-Means and Agglomerative Clustering

## Clustering Methods

### K-Means

K-Means was used to segment candidates based on similarities across their standardized characteristics.

A two-cluster solution produced a silhouette score of approximately **0.233** and provided a simple, interpretable segmentation of the candidate population.

### Agglomerative Clustering

Agglomerative Clustering was also applied using Ward linkage.

The two-cluster Agglomerative solution produced a silhouette score of approximately **0.205**.

| Method | Number of Clusters | Silhouette Score |
|---|---:|---:|
| K-Means | 2 | 0.233 |
| Agglomerative Clustering | 2 | 0.205 |

## Key Findings

The K-Means solution identified two distinct candidate segments:

- **Cluster 0:** More experienced candidates who generally work at larger companies and have gone longer since their most recent job change. This group had a job-change rate of approximately **9.9%**.
- **Cluster 1:** Less-experienced candidates who generally work at somewhat smaller companies and have changed jobs more recently. This group had a substantially higher job-change rate of approximately **23.1%**.

Although larger values of `k` produced somewhat higher silhouette scores, the two-cluster solution was retained because it provided a simpler and more interpretable segmentation.

Because the target variable was not used to construct the clusters, the difference in job-change rates provides an external perspective on the candidate segments discovered through unsupervised learning.

## Key Techniques

- Unsupervised Learning
- K-Means Clustering
- Agglomerative Clustering
- Feature Standardization
- Elbow Method
- Silhouette Analysis
- Hierarchical Clustering
- Dendrogram Analysis
- Cluster Profiling

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy
- Jupyter Notebook

## Project File

- `hr_candidate_clustering.ipynb`
