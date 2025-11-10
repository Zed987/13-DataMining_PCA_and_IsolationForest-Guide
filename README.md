
<br>

**\[[🇧🇷 Português](README.pt_BR.md)\] \[**[🇺🇸 English](README.md)**\]**





<br><br>

# 13- [Data Mining]()  / [Principal Component Analysis (PCA) and Isolation Forest Algorithms]()

### <p align="center"> _A practical guide to dimensionality reduction and anomaly detection. An easy guide for everyone !_

<br><br>

This repository provides a hands-on guide to two powerful data mining techniques — **Principal Component Analysis (PCA)** and **Isolation Forest**.  
It explains how to simplify high-dimensional data and detect outliers with visual and practical examples.  

<br><br>

#### <p align="center"> [![Sponsor Quantum Software Development](https://img.shields.io/badge/Sponsor-Quantum%20Software%20Development-brightgreen?logo=GitHub)](https://github.com/sponsors/Quantum-Software-Development)



<!-- ======================================= Start DEFAULT HEADER ===========================================  -->

<br><br><br>


[**Institution:**]() Pontifical Catholic University of São Paulo (PUC-SP)  
[**School:**]() Faculty of Interdisciplinary Studies  
[**Program:**]() Humanistic AI and Data Science
[**Semester:**]() 2nd Semester 2025  
Professor:  [***Professor Doctor in Mathematics Daniel Rodrigues da Silva***](https://www.linkedin.com/in/daniel-rodrigues-048654a5/)

<br><br><br><br>



<!-- PUC HEADER GIF
<p align="center">
  <img src="https://github.com/user-attachments/assets/0d6324da-9468-455e-b8d1-2cce8bb63b06" />
-->


<!-- video presentation -->


##### 🎶 Prelude Suite no.1 (J. S. Bach) - [Sound Design Remix]()

https://github.com/user-attachments/assets/4ccd316b-74a1-4bae-9bc7-1c705be80498

####  📺 For better resolution, watch the video on [YouTube.](https://youtu.be/_ytC6S4oDbM)


<br><br><br>



> [!TIP]
> 
>  This repository is a review of the Statistics course from the undergraduate program Humanities, AI and Data Science at PUC-SP.
>
> ### ☞ **Access Data Mining [Main Repository](https://github.com/Quantum-Software-Development/1-Main_DataMining_Repository)**
>
>


<br><br><br>


<!-- =======================================END DEFAULT HEADER ===========================================  -->

#

<!--Confidentiality statement -->


<br><br><br>

> [!IMPORTANT]
> 
> ⚠️ Heads Up
>
> * Projects and deliverables may be made [publicly available]() whenever possible.
> * The course emphasizes [**practical, hands-on experience**]() with real datasets to simulate professional consulting scenarios in the fields of **Data Analysis and Data Mining** for partner organizations and institutions affiliated with the university.
> * All activities comply with the [**academic and ethical guidelines of PUC-SP**]().
> * Any content not authorized for public disclosure will remain [**confidential**]() and securely stored in [private repositories]().  
>


<br><br>



<!--END-->



## Table of Contents

- [Introduction](#introduction)  
- [What is PCA?](#what-is-pca)  
- [How does PCA Work?](#how-does-pca-work)  
- [What is the Isolation Forest Algorithm?](#what-is-the-isolation-forest-algorithm)  
- [How does Isolation Forest Work?](#how-does-isolation-forest-work)  
- [Steps to Prepare Your Dataset (Data Cleaning)](#steps-to-prepare-your-dataset-data-cleaning)  
- [Data Normalization and Feature Scaling](#data-normalization-and-feature-scaling)  
- [Visualizations: Scatter Plots and Box Plots](#visualizations-scatter-plots-and-box-plots)  
- [Dimensionality Reduction Comparison: PCA vs. t-SNE](#dimensionality-reduction-comparison-pca-vs-t-sne)  
- [How to Choose the Right Algorithm](#how-to-choose-the-right-algorithm)  
- [Spiral-shaped Datasets: K-Means vs. DBSCAN](#spiral-shaped-datasets-k-means-vs-dbscan)  
- [Evaluation Metrics for Clustering and Anomaly Detection](#evaluation-metrics-for-clustering-and-anomaly-detection)  
- [Code Implementation](#code-implementation)  
- [Results and Insights](#results-and-insights)  
- [Conclusion](#conclusion)  
- [References](#references)


<br><br>

#  [Introduction]()

This project introduces core **Data Mining** concepts using simple, interpretable examples in Python.  

It demonstrates how to clean data, reduce dimensionality using **PCA**, and detect anomalies with **Isolation Forest**.

All code examples are easy to follow and include visualizations for learning and experimentation.


<br><br>


## [What is PCA ?]()

**PCA (Principal Component Analysis)** simplifies large datasets by keeping the most important patterns while reducing noise and redundancy.  

It’s like summarizing a book: you lose the extra words but keep the full meaning.


<br><br>


##  [How does PCA work ?]()

[1](). Center and normalize your data.  
[2](). Compute covariance matrix.  
[3](). Extract eigenvectors (principal components).  
[4](). Keep the top components explaining most of the variance.  
[5](). Visualize results using biplots or scree plots.


<br><br>


## [What is the Isolation Forest Algorithm ?]()

**Isolation Forest** is used for **anomaly detection** — spotting items that differ significantly from the majority.  

It isolates anomalies by randomly splitting data and measuring how quickly a sample can be separated.


<br><br>

## [How does Isolation Forest Work ?]() 

[1]() . Build multiple random trees.  
[2]() . Each split isolates points based on random features.  
[3]() . Fewer splits = more likely an anomaly.  
[4]() . Compute anomaly scores and visualize them.


<br><br>

## 🧹 [Steps to Prepare Your Dataset (Data Cleaning)]()

[-]() Remove missing or duplicate values.  
[-]() Normalize and scale features.  
[-]() Visualize your dataset with **scatter** and **box plots** to spot trends and outliers.


<br><br>

##  [Data Normalization and Feature Scaling]()

Scaling ensures that all features contribute equally to the analysis.  

Use **StandardScaler** or **MinMaxScaler** from `sklearn.preprocessing`.


<br><br>

## [Visualizations: Scatter Plots and Box Plots]()

Visual tools help interpret the structure of your data and spot anomalies.

<br>

```python
import matplotlib.pyplot as plt
import seaborn as sns

sns.scatterplot(x='feature1', y='feature2', data=df)
plt.title("Scatter Plot Example")
plt.show()
```

<br><br>

## [How to Choose the Right Algorithm]()

[-]() For structured numeric data → use PCA

[-]() For anomaly detection → use Isolation Forest

[-]() For non-linear structures → try t-SNE or DBSCAN

[-]() For spiral or irregular data → prefer DBSCAN over K-Means


<br><br>

## 🔬 [Dimensionality Reduction Comparison: PCA vs. t-SNE]()

<br>

| [Method]()             | [Type]()        | [Use Case]()                               | [Notes]()                                      |
|-------------------|------------|----------------------------------------|--------------------------------------------|
| [PCA]()               | Linear     | Large, structured datasets             | Fast, interpretable, reduces dimensionality |
| [t-SNE]()             | Non-linear | Visualizing high-dimensional data      | Better for clusters, slower                 |
| [Isolation Forest]()  | Unsupervised| Outlier / anomaly detection            | Works well with high-dimensional data, unsupervised |
| [DBSCAN]()            | Clustering | Detecting clusters of arbitrary shape | Does not require number of clusters, handles noise |
| [K-Means]()           | Clustering | Partitioning data into k clusters      | Assumes spherical clusters, fast on large datasets |


<br><br>

## 🌀 [Spiral-shaped Datasets: K-Means vs. DBSCAN]()

[-]()  ***K-Means*** assumes circular clusters — not good for complex shapes.

[-]()  ***DBSCAN*** can detect arbitrary-shaped clusters (e.g., spirals) and noise.


<br><br>

## [PCA Implementation (Code + Visualization)]()

Here’s a simple example of PCA using the Iris dataset:

<br>

```python
from sklearn.decomposition import PCA
from sklearn.datasets import load_iris
from sklearn.preprocessing import StandardScaler
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
iris = load_iris()
X = iris.data
y = iris.target

# Standardize
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Apply PCA
pca = PCA(n_components=2)
X_pca = pca.fit_transform(X_scaled)

# Visualize
plt.figure(figsize=(8,6))
sns.scatterplot(x=X_pca[:,0], y=X_pca[:,1], hue=y, palette='viridis', s=100)
plt.xlabel("Principal Component 1")
plt.ylabel("Principal Component 2")
plt.title("PCA Projection of Iris Dataset")
plt.show()
```

<br>

### 🔗 Notebook completo: [PCA_Analysis.ipynb](https://github.com/Quantum-Software-Development/13-DataMining_PCA_and_IsolationForest-Guide/blob/07be5a419f1e86c7cf02f417171896a2f549a2f6/Component%20Analysis%20(PCA)/Code/PCA_Based_Image_Code_Generation.ipynb)


<br><br>

## [Isolation Forest Implementation (Code + Results)]()

Example using synthetic data:

<br>


```python
from sklearn.ensemble import IsolationForest
import numpy as np
import matplotlib.pyplot as plt

# Generate synthetic data
rng = np.random.RandomState(42)
X = 0.3 * rng.randn(100, 2)
X_outliers = rng.uniform(low=-4, high=4, size=(20, 2))
X = np.r_[X + 2, X - 2, X_outliers]

# Fit the model
clf = IsolationForest(contamination=0.1, random_state=rng)
clf.fit(X)

# Predict anomalies
y_pred = clf.predict(X)

# Visualization
plt.scatter(X[:, 0], X[:, 1], c=y_pred, cmap='coolwarm')
plt.title("Isolation Forest - Anomaly Detection")
plt.show()
```


<br>

### 🔗 Notebook completo: [IsolationForest_Detection.ipynb](https://github.com/Quantum-Software-Development/13-DataMining_PCA_and_IsolationForest-Guide/blob/c855c0637f8b7b58dac3af705488b4f4c7e560b8/Isolation%20Forest%20Outlier%20Detection/Code/Isolation_Forest_Outlier_Detection.ipynb)

<br><br>




## ⚗️ [Interactive Notebooks]()

<br>

| [Notebook]() | [Google Colab]() | [Binder]() |
|-----------|---------------|---------|
| PCA Analysis | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Quantum-Software-Development/13-DataMining_PCA_and_IsolationForest-Guide/blob/main/notebooks/PCA_Analysis.ipynb) | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Quantum-Software-Development/13-DataMining_PCA_and_IsolationForest-Guide/HEAD?labpath=notebooks%2FPCA_Analysis.ipynb) |
| Isolation Forest | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Quantum-Software-Development/13-DataMining_PCA_and_IsolationForest-Guide/blob/main/notebooks/IsolationForest_Detection.ipynb) | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Quantum-Software-Development/13-DataMining_PCA_and_IsolationForest-Guide/HEAD?labpath=notebooks%2FIsolationForest_Detection.ipynb) |























<!-- ========================== [Bibliographr ====================  -->

<br><br>


## [Bibliography]()

<br>

[1]() **Abdi, H. & Williams**C, L.J. Principal Component Analysis. Wiley Interdisciplinary Reviews, 2010.

[2](). **Castro, L. N. & Ferrari, D. G.** (2016). *Introdução à mineração de dados: conceitos básicos, algoritmos e aplicações*. Saraiva.

[3](). **Dunteman**, J. Principal Component Analysis. SAGE Publications, 1989.

[4](). **Ferreira, A. C. P. L. et al.** (2024). *Inteligência Artificial - Uma Abordagem de Aprendizado de Máquina*. 2nd Ed. LTC.

[5](). **Larson & Farber** (2015). *Estatística Aplicada*. Pearson.

[6](). **Liu**, F.T. et al. Isolation Forest. IEEE ICDM, 2008.



<!-- ======================================= Start Footer ===========================================  -->


<br><br>


## 💌 [Let the data flow... Ping Me !](mailto:fabicampanari@proton.me)

<br><br>



#### <p align="center">  🛸๋ My Contacts [Hub](https://linktr.ee/fabianacampanari)


<br>

### <p align="center"> <img src="https://github.com/user-attachments/assets/517fc573-7607-4c5d-82a7-38383cc0537d" />




<br><br><br>

<p align="center">  ────────────── 🔭⋆ ──────────────


<p align="center"> ➣➢➤ <a href="#top">Back to Top </a>

<!--
<p align="center">  ────────────── ✦ ──────────────
-->



<!-- Programmers and artists are the only professionals whose hobby is their profession."

" I love people who are committed to transforming the world "

" I'm big fan of those who are making waves in the world! "

##### <p align="center">( Rafael Lain ) </p>   -->

#

###### <p align="center"> Copyright 2025 Quantum Software Development. Code released under the [MIT License license.](https://github.com/Quantum-Software-Development/Math/blob/3bf8270ca09d3848f2bf22f9ac89368e52a2fb66/LICENSE)











