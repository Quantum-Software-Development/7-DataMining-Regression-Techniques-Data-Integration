
<br>

**\[[🇧🇷 Português](README.pt_BR.md)\] \[**[🇺🇸 English](README.md)**\]**


<br><br>

# 7- [Data Mining]() / Regression Techniques with Data Integration


<!-- ======================================= Start DEFAULT HEADER ===========================================  -->

<br><br>


[**Institution:**]() Pontifical Catholic University of São Paulo (PUC-SP)  
[**School:**]() Faculty of Interdisciplinary Studies  
[**Program:**]() Humanistic AI and Data Science
[**Semester:**]() 2nd Semester 2025  
Professor:  [***Professor Doctor in Mathematics Daniel Rodrigues da Silva***](https://www.linkedin.com/in/daniel-rodrigues-048654a5/)

<br><br>

#### <p align="center"> [![Sponsor Quantum Software Development](https://img.shields.io/badge/Sponsor-Quantum%20Software%20Development-brightgreen?logo=GitHub)](https://github.com/sponsors/Quantum-Software-Development)


<br><br>

<!--Confidentiality statement -->

#

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

#

<!--END-->




<br><br><br><br>



<!-- PUC HEADER GIF
<p align="center">
  <img src="https://github.com/user-attachments/assets/0d6324da-9468-455e-b8d1-2cce8bb63b06" />
-->


<!-- video presentation -->


##### 🎶 Prelude Suite no.1 (J. S. Bach) - [Sound Design Remix]()

https://github.com/user-attachments/assets/4ccd316b-74a1-4bae-9bc7-1c705be80498

####  📺 For better resolution, watch the video on [YouTube.](https://youtu.be/_ytC6S4oDbM)


<br><br>


> [!TIP]
> 
>  This repository is a review of the Statistics course from the undergraduate program Humanities, AI and Data Science at PUC-SP.
>
>  ### ☞ **Access Data Mining [Main Repository](https://github.com/Quantum-Software-Development/1-Main_DataMining_Repository)**
> 
>

<!-- =======================================END DEFAULT HEADER ===========================================  -->

<br><br>



## [Overview]()

This repository covers fundamental concepts and practical techniques in Data Mining focused on clustering (grouping by similarity), various types of regression for modeling data trends, and the crucial steps for data integration and preprocessing. Each section includes theoretical explanations, use case examples, mathematical formulations using LaTeX, and Python code snippets to assist practical understanding.

<br><br>

## [Table of Contents]()

- [Clustering](#clustering)
- [Regression Types](#regression-types)
- [Data Integration](#data-integration)
    - [Data Redundancy and Duplicates](#data-redundancy-and-duplicates)
    - [Data Conflicts](#data-conflicts)
    - [Data Compression](#data-compression)
    - [PCA - Principal Component Analysis](#pca)
    - [Data Standardization](#data-standardization)
    - [Data Normalization](#data-normalization)


<br><br>

## [Clustering]()

Clustering is a technique to group data points that are similar and separate those that are different. Similarity is often measured numerically using distances in a coordinate space.

<br>

### [Euclidean Distance Formula]()

<br>

The most common distance metric used is Euclidean distance between two points $a = (a_1, a_2, ..., a_n)$ and $b = (b_1, b_2, ..., b_n)$:

<br><br>

$$
\Huge
d(a, b) = \sqrt{\sum_{i=1}^n (a_i - b_i)^2}
$$

<br><br>

```latex
d(a, b) = \sqrt{\sum_{i=1}^n (a_i - b_i)^2}
```

<br><br>

> *This distance represents the shortest straight line distance between two points in n-dimensional space, calculated using the Pythagorean theorem.*


<br><br>


## [Use Case Example]()

<br>

Suppose you want to segment customers into groups based on age, income, and spending score to personalize marketing strategies. Clustering algorithms group similar customers by minimizing their Euclidean distances within clusters.

<br><br>


## [Regression Types]()

<br>

Regression models describe the relationship between a dependent variable and one or more independent variables, often used to predict trends or outcomes.

<br> 

### [*Importance of Scatter Plots*]()

Before selecting a regression model, it is essential to plot a scatter plot of the data to understand how points are distributed and determine the best fitting model. The scatter plot reveals if data follows linear, exponential, polynomial, or logistic patterns.

<br><br>

## [Common Regression Types]()

<br><br>

| [Regression Type]() | [Description]() | [Equation / Model]() |
| :-- | :-- | :-- |
| [Linear Regression]() | Models data with a straight line, assumes linear relationship. | \$y = \beta_0 + \beta_1 x \$ |
| [Polynomial Regression]() | Fits a polynomial curve, useful for nonlinear trends. | \$y = \beta_0 + \beta_1 x + \beta_2 x^2 + \cdots + \beta_n x^n \$ |
| [Logarithmic Regression]() | Models data with logarithmic growth or decay. | \$y = \beta_0 + \beta_1 \log(x) \$ |
| [[Exponential Regression]() | Models exponential increase or decrease. | \$y = \beta_0 e^{\beta_1 x} \$ |
| [Logistic Regression]() | Used for predicting binary outcomes, S-shaped curve. | \$p = \frac{1}{1 + e^{-(\beta_0 + \beta_1 x)}} \$ |


<br><br>

## [Data Integration]()

<br>

In real-world applications, data often comes from various sources and needs to be integrated into a consistent dataset ready for mining and modeling.

<br>

### [*Data Redundancy and Duplicates*]()

Redundancy occurs when the same data appears multiple times, which can bias analysis or cause inconsistencies. A common case is duplicate rows in datasets.

<br>

### [*Python Code to Detect and Remove Duplicates*]()

<br>

```python
# Code to detect duplicates and remove them
import pandas as pd

df = pd.read_csv('/content/cancer.csv')
print(df.duplicated().value_counts())

# Remove duplicates
df_clean = df.drop_duplicates()
```

<br><br>


## Data Conflicts

Data conflicts arise when different sources provide inconsistent values for the same entity, for example, distances in kilometers vs miles or weights in kilograms vs pounds. Resolving conflicts often requires standardization to consistent units and formats.

<br><br>


## Data Compression

Compression reduces data dimensionality or size to improve efficiency without losing essential information. Two main approaches:

- **Attribute Compression:** Encoding or transforming attributes (e.g., PCA).

- **Data Reduction:** Removing or summarizing instances or attributes.

  
<br><br>

## PCA - Principal Component Analysis

PCA transforms correlated variables into a set of linearly uncorrelated components that capture the most variance in the data.

  
<br><br>

## Data Standardization

Standardization addresses differences in units and scales, converting data to a common format—for example, capitalizing strings to avoid case-sensitive mismatches or converting dates to a consistent format.

  
<br><br>

## Data Normalization

Normalization rescales numerical attributes so all variables have the same domain, essential for distance-based algorithms like clustering or neural networks.




























<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>


<!-- ========================== [Bibliographr ====================  -->


## [Bibliography]()

[1](). **Castro, L. N. & Ferrari, D. G.** (2016). *Introduction to Data Mining: Basic Concepts, Algorithms, and Applications*. Saraiva.

[2](). **Ferreira, A. C. P. L. et al.** (2024). *Artificial Intelligence – A Machine Learning Approach*. 2nd Ed. LTC.

[3](). **Larson & Farber** (2015). *Applied Statistics*. Pearson.


      
<!-- ======================================= Bibliography Portugues ===========================================  -->

<!--

## [Bibliography]()


[1](). **Castro, L. N. & Ferrari, D. G.** (2016). *Introdução à mineração de dados: conceitos básicos, algoritmos e aplicações*. Saraiva.

[2](). **Ferreira, A. C. P. L. et al.** (2024). *Inteligência Artificial - Uma Abordagem de Aprendizado de Máquina*. 2nd Ed. LTC.

[3](). **Larson & Farber** (2015). *Estatística Aplicada*. Pearson.


<br><br>
-->


<br><br>


<!-- ======================================= Start Footer ===========================================  -->


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











