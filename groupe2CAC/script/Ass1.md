# 🧾 Assignment 1 – Ayoub ENOUJAI

<img src="AYOUB PIC.jpg" style="height:464px;margin-right:432px"/>

---


N:APOGGEE : 22007782

## 👨‍🎓 Étudiant à l’ENCG Settat – Groupe 2 CAC  
**Spécialité : controle audit et conseil Gestion – Semestre 3**

---

# 🍷 Wine Quality Dataset

## 🧾 Overview
The **Wine Quality Dataset** is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality).  
It contains data on the **physicochemical properties** of *red* and *white* wines from the **Vinho Verde** region in northern Portugal.  
The dataset’s main goal is to explore the relationship between **objective chemical tests** and **subjective sensory quality ratings**.

---

## 📦 Dataset Summary

| Property | Description |
|-----------|-------------|
| **Name** | Wine Quality |
| **Source** | UCI Machine Learning Repository |
| **Region** | Vinho Verde (Northern Portugal) |
| **Datasets** | 2 (Red wine and White wine) |
| **Instances** | 1,599 (red) + 4,898 (white) |
| **Features** | 11 input variables + 1 output (quality) |
| **Task Type** | Regression or Classification |
| **Missing Values** | None |
| **License** | Creative Commons Attribution 4.0 (CC BY 4.0) |

---

## ⚗️ Input Variables (Physicochemical Tests)

| No. | Variable | Description |
|-----|-----------|-------------|
| 1 | `fixed_acidity` | Non-volatile acids such as tartaric and malic acids that do not evaporate easily. |
| 2 | `volatile_acidity` | Acetic acid content; high values can produce a vinegar taste. |
| 3 | `citric_acid` | Adds freshness and flavor; acts as a preservative. |
| 4 | `residual_sugar` | Amount of sugar left after fermentation; determines wine sweetness. |
| 5 | `chlorides` | Salt content in the wine. |
| 6 | `free_sulfur_dioxide` | SO₂ that can react with oxygen to prevent oxidation and microbial growth. |
| 7 | `total_sulfur_dioxide` | Sum of free and bound SO₂; excessive amounts can affect aroma. |
| 8 | `density` | Related to the sugar and alcohol content of the wine. |
| 9 | `pH` | Describes how acidic or basic a wine is (lower = more acidic). |
| 10 | `sulphates` | Contribute to sulfur dioxide levels; act as preservatives. |
| 11 | `alcohol` | Alcohol percentage by volume. |

---

## 🎯 Output Variable (Sensory Quality)

| Variable | Description |
|-----------|-------------|
| `quality` | Wine quality score between **0 and 10**, as rated by professional tasters. Usually ranges from **3 to 8**. |

---

## 🧠 Notes and Insights

- The `quality` variable is **ordinal** (higher = better), but **class distribution is imbalanced** — most wines are of medium quality.
- There are **no missing values**, making it suitable for both statistical and machine learning tasks.
- The dataset can be analyzed separately for **red** and **white** wines, or combined with an added categorical variable (`type`).
- Because taste is subjective, correlations between physicochemical variables and quality may be weak or nonlinear.

---

# 🧪 Wine Quality Analysis — Code Summary

This notebook analyzes the **Wine Quality dataset** (from the UCI Machine Learning Repository).  
You have already documented the dataset and its variables, so this summary focuses on the **code workflow and visualization process**.

---

## 📦 1. Importing and Fetching the Dataset

```python
!pip install ucimlrepo
from ucimlrepo import fetch_ucirepo

# Fetch dataset
wine_quality = fetch_ucirepo(id=186)

# Extract features and targets
X = wine_quality.data.features
y = wine_quality.data.targets

# Display metadata and variable info
print(wine_quality.metadata)
print(wine_quality.variables)


---

```

## 📦 2. Data presentation


This histogram visualizes the frequency of each wine quality score. You can see which scores are most common and the overall distribution of quality in the dataset.


INSERT IMAGE HERE


These box plots visualize the distribution of each physicochemical input feature across different wine quality scores. This can help identify which features tend to have higher or lower values for wines with better or worse quality, suggesting potential relationships between the features and the target variable.



INSERT IMAGE 2 HERE


These scatter plots illustrate the relationship between two input features, with the points colored according to the wine quality score. This can reveal patterns, clusters, or trends where certain combinations of feature values are associated with higher or lower quality wines. For instance, you might observe regions in the plot where high-quality wines tend to cluster, indicating optimal ranges for these feature pairs.



INSERT IMAGE 3 



This heatmap displays the pairwise correlation coefficients between all the features and the target variable ('quality').

Color Intensity: Stronger colors (closer to dark red or dark blue) indicate stronger correlations.
Color Hue: Red hues indicate positive correlations (as one variable increases, the other tends to increase), while blue hues indicate negative correlations (as one variable increases, the other tends to decrease).
Numbers: The annotated numbers are the correlation coefficients, ranging from -1 (perfect negative correlation) to 1 (perfect positive correlation), with 0 indicating no linear correlation.
This plot is useful for quickly identifying which features might be strongly predictive of wine quality, or which features are highly correlated with each other (which could indicate multicollinearity).




hese violin plots compare the distributions of each physicochemical feature for red versus white wines. Each plot shows the density estimation of the feature's values for each wine color, allowing you to easily see differences in median, spread, and overall shape of the distributions between the two types of wine. This can highlight features that are distinct characteristics of red or white wines.


INSERT IMAGE 4 



These bar charts display the average value of each physicochemical feature for each wine quality score. This visualization helps to clearly see trends: whether the average of a particular feature generally increases, decreases, or stays relatively stable as the wine quality improves or declines. This can provide direct insights into which chemical properties are most strongly associated with different quality ratings.



INSERT IMAGE 5



















