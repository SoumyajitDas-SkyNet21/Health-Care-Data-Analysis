🏥 Healthcare Data Analysis Using Python (Pandas)
This project explores a synthetic healthcare dataset containing patient records to uncover insights using Pandas. The dataset contains 500+ patient entries with various attributes such as age, gender, department, diagnosis, treatment cost, and outcomes.

📊 Business Questions & Insights
1. What is the Average Age of Patients?
python
Copy
Edit
health_data['Age'].mean()
📌 Insight: The average age of patients is 51.66 years.

2. What is the Gender Distribution of Patients?
python
Copy
Edit
health_data['Gender'].value_counts(normalize=True) * 100
📌 Insight:

Female: 41.63%

Male: 39.63%

Other: 18.73%

Majority of patients are female.

3. Top 5 Cities with the Highest Number of Patients
python
Copy
Edit
health_data['City'].value_counts().head(5)
📌 Insight: Lake David, Smithshire, East Christopher, Christopherville, and Brownburgh lead in patient count.

4. Number of Patients Admitted per Department
python
Copy
Edit
health_data['Department'].value_counts()
📌 Insight: Most admissions were in Pediatrics, followed by Gastroenterology and Neurology.

5. Average Length of Stay per Department
python
Copy
Edit
health_data.groupby('Department')['Length_of_Stay'].mean()
📌 Insight: Stays range from 14 to 17 days across departments, with Gastroenterology having the highest average.

6. What is the Overall Average Treatment Cost?
python
Copy
Edit
health_data['Treatment_Cost'].mean()
📌 Insight: ₹10,359 is the overall average treatment cost.

7. Average Treatment Cost by Department
python
Copy
Edit
health_data.groupby('Department')['Treatment_Cost'].mean()
📌 Insight:

Highest: Oncology (₹11,042)

Lowest: Cardiology (₹9,781)

8. Top 3 Most Common Diagnoses
python
Copy
Edit
health_data['Diagnosis'].value_counts().head(3)
📌 Insight:

Fracture

Tuberculosis

Migraine

9. Readmission Rate Within 30 Days
python
Copy
Edit
health_data['Readmission_Within_30_Days'].value_counts(normalize=True) * 100
📌 Insight: ~17.46% of patients were readmitted within 30 days.

10. Department with Highest Avg. Treatment Cost
python
Copy
Edit
health_data.groupby('Department')['Treatment_Cost'].mean().idxmax()
📌 Insight: Oncology tops in cost.

11. Correlation Between Age and Treatment Cost
python
Copy
Edit
health_data['Age'].corr(health_data['Treatment_Cost'])
📌 Insight: Weak negative correlation (-0.041). Age doesn't significantly affect cost.

12. Distribution of Payment Methods
python
Copy
Edit
health_data['Payment_Method'].value_counts()
📌 Insight:

Insurance: 161

Medicare: 141

Credit Card: 124

Cash: 118

13. City with Highest Avg. Treatment Cost
python
Copy
Edit
health_data.groupby('City')['Treatment_Cost'].mean().idxmax()
📌 Insight: Kevinberg has the highest average treatment cost.

14. Avg. Length of Stay by Diagnosis
python
Copy
Edit
health_data.groupby('Diagnosis')['Length_of_Stay'].mean()
📌 Insight:

Longest: Arthritis, Fracture (18 days)

Shortest: Migraine (12 days)

15. Do Older Patients (60+) Have Higher Readmission Rates?
python
Copy
Edit
# Compare readmission for age >60 and <60
📌 Insight:

60 years: 13.9%

<60 years: 20.2%

Surprisingly, younger patients had higher readmission rates.

16. Department-wise Mortality Rate Analysis
python
Copy
Edit
# Deceased count / total per department
📌 Insight:

Highest mortality: Orthopedics (44.77%)

Lowest mortality: Gastroenterology (25.88%)

📌 Summary & Key Learnings
The average patient age is ~52 years with female patients slightly outnumbering males.

Fracture, Tuberculosis, and Migraine are the most common diagnoses.

Oncology stands out with the highest treatment cost.

A notable 17.5% readmission rate exists within 30 days.

Mortality rates differ significantly by department, warranting further attention.

Younger patients had higher readmission rates than expected.

📁 Tools & Technologies Used
Python

Pandas

Jupyter Notebook

Matplotlib / Seaborn (Optional for visualization)

✅ Next Steps (Optional Ideas)
Build interactive dashboards using Power BI or Plotly Dash

Perform predictive modeling on readmission or mortality

Add visualizations to support your findings

