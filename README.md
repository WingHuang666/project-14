# project-14

# Mushroom Classification and Clustering Analysis

## Project Overview

This project analyzes mushroom characteristics to investigate patterns associated with edible and poisonous mushrooms. The dataset contains categorical characteristics describing mushroom appearance, structure, odor, population, and habitat.

The project combines supervised machine learning and unsupervised clustering to answer five research questions. Classification models are used to predict mushroom toxicity under different feature settings, while K-Means clustering is used to identify natural mushroom groups and compare their toxicity profiles.

## Dataset

The dataset contains 8,124 mushroom observations with 23 variables:

- 1 target variable: `class`
- 22 predictor variables

The target variable contains two classes:

- `e` = Edible
- `p` = Poisonous

The predictor variables describe:

- Cap characteristics
- Odor and bruising
- Gill characteristics
- Stalk characteristics
- Veil and ring characteristics
- Spore-print color
- Population
- Habitat

All predictor variables are categorical. Missing values represented by `?` in `stalk-root` are treated as missing data and imputed using the most frequent category.

## Research Questions

### RQ1: Can mushroom characteristics accurately predict whether a mushroom is edible or poisonous?

Five classification models were compared:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- Support Vector Machine



### RQ2: Can mushroom toxicity still be predicted accurately without using odor?

The odor variable was removed and the classification models were retrained.


### RQ3: Can cap characteristics alone predict whether a mushroom is poisonous?

Only the following characteristics were used:

- Cap shape
- Cap surface
- Cap color


### RQ4: Can habitat and population characteristics predict mushroom toxicity?

Only `habitat` and `population` were used as predictors.


### RQ5: Are there naturally occurring mushroom groups, and do these groups have different poisoning rates?

K-Means clustering was applied to the one-hot encoded mushroom characteristics without using the edible/poisonous target variable.

The Elbow Method and Silhouette Score were used together to evaluate the number of clusters.



## Feature Importance

## Methods

### Data Preprocessing

- Missing-value handling with `SimpleImputer`
- One-hot encoding for categorical variables
- Stratified train/test split
- Poisonous mushrooms treated as the positive class

### Classification Models

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- Support Vector Machine

Classification performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC AUC
- Confusion Matrix

### Clustering

- One-Hot Encoding
- K-Means
- Elbow Method
- Silhouette Score
- PCA visualization
- Cluster toxicity profiling
- Categorical cluster profiling
