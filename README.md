# CSC2042S 2025 – Assignment 1: Unsupervised Learning
## This assignment is primarily for doing PCA and K-means
**Below are the libraries used**
**import numpy as np** 
**import pandas as pd**  
**import matplotlib.pyplot as plt**
**from sklearn.decomposition import PCA**  
**from sklearn.manifold import TSNE**

**The notebook submitted does the foolowing tasks**  
## 1.Data Preprocessing (Please note in this section the notebook will write the processed data into the current work folder (helps with seeing the data in tabular format))
**steps:**   
**1.Load the dataset**  
**2.Melt and Pivot the dataset to get into good structure of each row representing COUNTRY/YEAR with multiple clumns(Indicators)**  
**3.Handle missing values by check various threshholds for wch we get a good balance between completness and coverage.**  
**4.Normalize features**  
**5.Save cleaned data for later use**

## PCA before kmeans
**The aim is to find the optimal number of dimesions to keep before applying the k-means** 

## 2. K-means Clustering and Initialization
**Compare the two methods of initialising my centroids**  
**I do the comparison for both the data with all of the indicators and the data with M=175 indicators to see if the PCA improves perfomance**

## 3. Convergence Criteria
**In this section :The aim is to implement and evaluate multiple different convergence criteria:**  
**maximum iterations**  
**centroid change threshold (when cluster centroids move less than a specified distance)**  
**And inertia change threshold (when the loss function improvement falls below a minimum value)**

## 5. Dimensionality Reduction with PCA
**-Use PCA to plot/visulise the data i have clustered(just when using t-SNE i will use vStack)**  
**-Visualizing both cases >>>2D and 3D**

# 7. Creative Extensions(I use silhoutte scores to plot and compare that to my loss function)