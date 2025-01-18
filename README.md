# Heart Attack Dataset Analysis: Insights on Youth and Adult Health in Germany

## Overview

This dataset provides valuable insights into the occurrence of heart attacks among individuals under 25 years (youth) and those 25 years and older (adults) across various states in Germany from 2015 to 2023. The data includes several health and lifestyle factors, such as hypertension, BMI (Body Mass Index), and socioeconomic status. The dataset is designed to encourage deeper exploration by being unevenly distributed, making the analysis more challenging and rewarding.

By analyzing this dataset, we aim to understand the factors contributing to heart attacks and uncover patterns that might be used for preventive measures.

---

## Dataset Details

- **Age Group**: Categories representing individuals' age:
  - **Under 25**
  - **25+ years**
  
- **Hypertension**: Whether the individual suffers from hypertension (High blood pressure).
  - **Yes**
  - **No**
  
- **Socioeconomic Status**: The socioeconomic status of the individual, which may correlate with heart health.
  - Categories: **Low**, **Medium**, **High**
  
- **BMI**: The Body Mass Index (BMI) of the individual, which is a common health indicator linked to heart disease risk.

---

## Data Visualizations

### 1. **Hypertension by Age Group**
This visualization explores how hypertension varies across different age groups. A **countplot** helps us compare the frequency of individuals with and without hypertension in the youth and adult categories.

![Hypertension by Age Group](heatmap.png)

```python
plt.figure(figsize=(8, 5))
sns.countplot(x='Age_Group', hue='Hypertension', data=data, palette='husl')
plt.title("Hypertension by Age Group")
plt.xlabel("Age Group")
plt.ylabel("Count")
plt.legend(title="Hypertension", labels=["No", "Yes"])
plt.show()
