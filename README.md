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

📌 Insight:

Female: 41.63%

Male: 39.63%

Other: 18.73%

Majority of patients are female.
```
<img src="./images/Gender_Distribution.png" alt="Gender Distribution Chart" width="400"/>

<img src="./images/Gender Distribution_Piechart.png" alt="Gender Distribution Chart" width="400"/>


### 3. Top 5 Cities with the Highest Number of Patients
```python
health_data['City'].value_counts().head(5)
📌 Insight:
Lake David, Smithshire, East Christopher, Christopherville, and Brownburgh lead in patient count.
```
<img src="./images/Top 5 Cities With Highest Number of Patients.png" alt="Gender Distribution Chart" width="400"/>

### 4. Number of Patients Admitted per Department
```
health_data['Department'].value_counts()
📌 Insight:
Most admissions were in Pediatrics, followed by Gastroenterology and Neurology.
```
<img src="./images/No. Of Patients Department Wise.png" alt="Gender Distribution Chart" width="400"/>

### 5. Average Length of Stay per Department
```health_data.groupby('Department')['Length_of_Stay'].mean()
📌 Insight:
Stays range from 14 to 17 days across departments, with Gastroenterology having the highest average.
```
### 6. What is the Overall Average Treatment Cost?
```
health_data['Treatment_Cost'].mean()
📌 Insight:
The overall average treatment cost is $ 10,359.
```
### 7. Average Treatment Cost by Department
```
health_data.groupby('Department')['Treatment_Cost'].mean()
📌 Insight:

Highest: Oncology ($11,042)

Lowest: Cardiology ($9,781)
```
### 8. Top 3 Most Common Diagnoses
```
health_data['Diagnosis'].value_counts().head(3)
📌 Insight:

Fracture
Tuberculosis
Migraine
```


