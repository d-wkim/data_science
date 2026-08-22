---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.19.4
kernelspec:
  name: python3
  display_name: Python 3 (ipykernel)
  language: python
---

# Machine Learning

+++

Notes from *Machine Learning with Python* (2nd edition).  
  
  
**Objective**: Learn and apply machine learning to systematic reviews and meta-analyses (https://doi.org/10.3390/bs15111476).

+++

**Table of Contents**

1. [Working with Vectors, Matrices, and Arrays in NumPy](#working-with-vectors-matrices-and-arrays-in-numpy)
2. [Loading Data](#loading-data)
3. [Data Wrangling](#data-wrangling)
4. [Handling Numerical Data](#handling-numerical-data)
5. [Handling Categorical Data](#handling-categorical-data)
6. [Handling Text Data](#handling-text)
7. [Handling Dates and Times](#handling-dates-and-times)
8. [Handling Images](#handling-images)
9. [Dimensionality Reduction Using Feature Extraction](#dimensionality-reduction-using-feature-extraction)
10. [Dimensionality Reduction Using Feature Selection](#dimensionality-reduction-using-feature-selection)
11. [Model Evaluation](#model-evaluation)
12. [Model Selection](#model-selection)
13. [Linear Regression](#linear-regression)
14. [Trees and Forests](#trees-and-forests)
15. [K-Nearest Neighbors](#k-nearest-neighbors)
16. [Logistic Regression](#logistic-regression)
17. [Support Vector Machines](#support-vector-machines)
18. [Naive Bayes](#naive-bayes)
19. [Clustering](#clustering)
20. [Tensors with PyTorch](#tensors-with-pytorch)
21. [Neural Networks](#neural-networks)
22. [Neural Networks for Unstructured Data](#neural-networks-for-unstructured-data)
23. [Saving, Loading, and Serving Trained Models](#saving-loading-and-serving-trained-models)

+++

## Working with Vectors, Matrices, and Arrays in NumPy

```{code-cell} ipython3

```

## Loading Data

```{code-cell} ipython3

```

## Data Wrangling

```{code-cell} ipython3

```

## Handing Numerical Data

```{code-cell} ipython3

```

## Handing Categorical Data

```{code-cell} ipython3

```

## Handling Text

```{code-cell} ipython3

```

## Handling Dates and Times

```{code-cell} ipython3

```

## Handling Images

```{code-cell} ipython3

```

## Dimensionality Reduction Using Feature Extraction

```{code-cell} ipython3

```

## Dimensionality Reduction Using Feature Selection

+++



+++

## Model Evaluation

```{code-cell} ipython3

```

## Model Selection

```{code-cell} ipython3

```

## Linear Regression

```{code-cell} ipython3

```

## Trees and Forests

```{code-cell} ipython3

```

## K-Nearest Neighbors

+++

k-nearest neighbors (KNN) classifier.

```{code-cell} ipython3
#!pip install -U scikit-learn
```

```{code-cell} ipython3
import datasets
from datasets import load_data
```

```{code-cell} ipython3
import pandas as pd

url = "https://raw.githubusercontent.com/d-wkim/data_science/refs/heads/main/datasets/"
datasets = ["cars", "housing", "loans"]

for dataset in datasets:
    url = f"https://raw.githubusercontent.com/d-wkim/data_science/refs/heads/main/datasets/data/{dataset}.csv"
    df = pd.read_csv(url, encoding = "utf-8")
    globals()[f"{dataset}"] = df
```

```{code-cell} ipython3
cars.head()
```

```{code-cell} ipython3
housing.head()
```

```{code-cell} ipython3
loans.head()
```

### 15. 1 Finding an Observation's Nearest Neighbors

+++

Don't be fooled again. 

```{code-cell} ipython3
from sklearn import datasets
from sklearn.neighbors import NearestNeighbors as NN
from sklearn.preprocessing import StandardScaler
```

```{code-cell} ipython3
standardizer = StandardScaler
features_
```

```{code-cell} ipython3
def KNN(dataset):
    import pandas as pd
    from sklearn.neighbors import NearestNeighbors as NN
    from sklearn.preprocessing import StandardScaler
    
    url = f"https://raw.githubusercontent.com/d-wkim/data_science/refs/heads/main/datasets/data/{dataset}.csv"
    df = pd.read_csv(url, encoding = "utf-8")
    df = df.fillna("")
    features = pd.DataFrame()

    for column in df.columns:
        if pd.api.types.is_float_dtype(df[column]) or pd.api.types.is_integer_dtype(df[column]):
            features[column] = df[column]

    scaler = StandardScaler()
    features_scaled = scaler.fit_transform(features)
    knn = NN(n_neighbors = 2)
    knn.fit(features_scaled)

    new = [[1, 1, 1, 1]]
    new_scaled = scaler.transform(new)
    
    distances, indices = knn.kneighbors(new_scaled)
    neighbors = df.iloc[indices[0]]
    print(neighbors)
```

### 15.2 Creating a K-Nearest Neighbors Classifier

```{code-cell} ipython3

```

### Identifying the Best Neighborhood Size

```{code-cell} ipython3

```

### Creating a Radius-Based Nearest Neighbors Classifier

```{code-cell} ipython3

```

### Finding Approximate Nearest Neighbors

```{code-cell} ipython3

```

### Evaluating Approximate Nearest Neighbors

```{code-cell} ipython3

```

## Logistic Regression

```{code-cell} ipython3

```

## Support Vector Machines

```{code-cell} ipython3

```

## Naive Bayes

```{code-cell} ipython3

```

## Clustering

```{code-cell} ipython3

```

## Tensors with PyTorch

```{code-cell} ipython3

```

## Neural Networks

```{code-cell} ipython3

```

## Neural Networks for Unstructured Data

```{code-cell} ipython3

```

## Saving, Loading, and Serving Trained Models

```{code-cell} ipython3

```
