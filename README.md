# Machin-Learning-ex3
college project, open to constructive comments.

# Clustering Algorithm Comparison on Synthetic Datasets

This repository contains a Python script for generating synthetic datasets with varying shapes (blobs, moons, and a ring) and applying and comparing different clustering algorithms. 
This project was developed as part of a college assignment focusing on unsupervised learning and cluster analysis.

## Project Overview

The goal of this project was to generate synthetic datasets with known underlying structures and evaluate the performance of various clustering algorithms.  
We explored K-Means, Hierarchical Agglomerative Clustering, and DBSCAN, analyzing their performance with different hyperparameters.

## Dataset Generation

The `generate_data.py` script creates synthetic datasets by combining three distinct components:

1. **Blobs:** Four Gaussian clusters are generated using `sklearn.datasets.make_blobs`.
2. **Moons:** Two intertwined crescent-shaped clusters are created using `sklearn.datasets.make_moons`.
3. **Ring:** A ring of points is generated using trigonometric functions and random noise.

The script allows control over the following parameters:

* `noise_level`: Controls the amount of noise added to the moons and the ring.
* `n_blobs`: Number of samples for the blobs.
* `n_moons`: Number of samples for the moons.
* `n_ring`: Number of samples for the ring.

## Clustering Algorithms

The following clustering algorithms were implemented and compared:

* **K-Means:**  A centroid-based algorithm that aims to partition the data into k clusters by minimizing the within-cluster variance.  Implemented using `sklearn.cluster.KMeans`.
* **Hierarchical Agglomerative Clustering:** A hierarchical clustering algorithm that builds a hierarchy of clusters by iteratively merging the closest clusters. Implemented using `sklearn.cluster.AgglomerativeClustering`.
* Different linkage methods (ward, complete, average, single) were experimented with.
* **DBSCAN (Density-Based Spatial Clustering of Applications with Noise):** A density-based clustering algorithm that identifies clusters based on the density of points. Implemented using `sklearn.cluster.DBSCAN`.  The `eps` and `min_samples` parameters were tuned.

## Experiments and Documentation

The `clustering_ex3.ipynb` notebook contains the code for running the clustering algorithms on the generated datasets and evaluating their performance.  The notebook includes:

* Data visualization for each dataset and clustering result.
* Evaluation metrics (e.g., Silhouette Score, adjusted Rand index - if ground truth labels are available).
  
The `Clustering Experiments.pdf` file contains the experiments' visualization and evaluation.
