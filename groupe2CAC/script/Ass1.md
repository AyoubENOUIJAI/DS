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

## 📊 Ideas for Visualization

Here are some basic charts you can build to explore and explain the dataset:

1. **Histogram of Quality Scores**
   - Shows the frequency of each quality rating.
   - Helps visualize class imbalance.

2. **Boxplots or Violin Plots**
   - Compare variables like `alcohol`, `sulphates`, or `volatile_acidity` across quality levels.

3. **Correlation Heatmap**
   - Displays pairwise correlations between features and `quality`.
   - Identifies which features are most strongly associated with quality.

4. **Scatter Plots**
   - Example: `alcohol` vs `density`, colored by `quality`.
   - Reveals patterns or clusters related to wine type or score.

5. **Bar Chart of Mean Feature Values by Quality Group**
   - Groups wines by low/medium/high quality and compares average feature values.

6. **Red vs White Comparison**
   - Overlay histograms or boxplots for red vs white wines on features like `pH`, `density`, or `residual_sugar`.

---

## 📚 References

- [UCI Machine Learning Repository — Wine Quality Dataset](https://archive.ics.uci.edu/dataset/186/wine+quality)  
- Cortez, P., Cerdeira, A., Almeida, F., Matos, T., & Reis, J. (2009).  
  *Modeling wine preferences by data mining from physicochemical properties.*  
  Decision Support Systems, 47(4), 547-553.

---
