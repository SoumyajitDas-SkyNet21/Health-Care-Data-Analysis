# 🏥 Healthcare Data Analysis Using Python (Pandas)

This project explores a synthetic healthcare dataset containing patient records to uncover insights using **Pandas**. The dataset contains 500+ patient entries with various attributes such as age, gender, department, diagnosis, treatment cost, and outcomes.

---

## 📊 Business Questions & Insights

### 1. What is the Average Age of Patients?
```python
health_data['Age'].mean()
📌 Insight: The average age of patients is 51.66 years.

```
### 2. What is the Gender Distribution of Patients?
```python

health_data['Gender'].value_counts(normalize=True) * 100
```python
📌 Insight:

Female: 41.63%

Male: 39.63%

Other: 18.73%

Majority of patients are female.

