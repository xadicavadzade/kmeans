# kmeans

# Customer Segmentation Analysis with Machine Learning


# Project Overview


This project implements comprehensive customer segmentation using various clustering algorithms to identify distinct customer groups based on demographic, behavioral, and spending patterns. The analysis helps businesses understand their customer base and develop targeted marketing strategies.


# Dataset Description


The dataset contains 8,068 customer records with 15 features including:


Customer Demographics


Age: Customer age


Work_Experience: Years of work experience


Family_Size: Number of family members


Gender_Male: Binary indicator for male gender


Ever_Married_Yes: Binary indicator for marriage status


Graduated_Yes: Binary indicator for graduation status


Customer Behavior & Preferences


Profession_B, Profession_C, Profession_D: One-hot encoded profession categories


Spending_Score_High, Spending_Score_Low: Customer spending behavior indicators


Var_1_B, Var_1_C, Var_1_D: Additional categorical variables


Target Variable


Segmentation: Original customer segments (A, B, C, D)


# Methodology


# 1. Data Preprocessing  


Loaded and examined 8,068 customer records
Applied data cleaning and preprocessing techniques
Handled categorical variables through one-hot encoding
Standardized features for clustering algorithms


# 2. Optimal Cluster Determination


Elbow Method


Tested K values from 2 to 9


Analyzed Within-Cluster Sum of Squares (WCSS)


Identified optimal number of clusters at the "elbow point"


Result: Inertia decreased from ~27,000 (K=2) to ~12,000 (K=9)


Silhouette Analysis


Evaluated cluster quality using silhouette coefficients


Tested multiple K values to find optimal clustering


Best silhouette score: ~0.25 for specific K values


Balanced between cluster separation and cohesion


# 3. Clustering Algorithms Implemented


K-Means Clustering (Primary Approach)


Applied K-means with optimal number of clusters


Generated comprehensive clustering results


Performance: Achieved well-separated customer segments


Alternative Clustering Methods


Hierarchical Clustering (Agglomerative)


Used Ward linkage for cluster formation


Provided dendogram-based cluster analysis


Results showed good separation across customer segments


DBSCAN (Density-Based Clustering)


Implemented with eps=0.5, min_samples=5


Identified clusters based on density patterns


Challenge: Generated many small clusters (100+ clusters)


Less suitable for this particular dataset structure


Gaussian Mixture Models (GMM)


Applied probabilistic clustering approach


Used multiple components for cluster identification


Provided probability-based cluster assignments


Semi-Supervised Clustering


Incorporated label spreading techniques


Combined supervised and unsupervised learning


# Result: Achieved perfect alignment with original segmentation
All diagonal elements in confusion matrix = 100%


Key Results


Model Performance Comparison


Algorithm


Performance


Best Use Case  


K-Means


# ✅ Good separation


Primary segmentation


Hierarchical


# ✅ Clear hierarchy


Understanding relationships


DBSCAN


# ⚠️ Over-segmented


Noise detection


GMM

# ✅ Probabilistic


Soft clustering


Semi-Supervised


# ✅ Perfect match


When labels available

Cluster Characteristics


The analysis identified distinct customer segments with varying:


Demographic profiles: Age, family size, education


Professional backgrounds: Different profession categories


Spending behaviors: High vs. low spending patterns


Geographic/behavioral variables: Additional distinguishing factors


Addressing Overfitting


Problem Identification


Initial clustering attempts showed signs of overfitting:


Too many small, non-meaningful clusters


Poor generalization to new data


High variance in cluster assignments


Solutions Implemented


Feature Selection: Reduced dimensionality to most relevant features


Cross-Validation: Validated cluster stability across data splits


Regularization: Applied appropriate parameter tuning


Ensemble Methods: Combined multiple clustering approaches


Silhouette Optimization: Used silhouette scores to prevent over-clustering


Final Model Selection


Selected K-means with optimal K based on elbow method and silhouette analysis


Balanced model complexity with interpretability


Achieved stable, meaningful customer segments


