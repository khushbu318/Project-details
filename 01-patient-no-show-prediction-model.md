# Patient No-Show Prediction Model

**Company:** Capgemini  
**Role:** Associate — Python Developer  
**Timeframe:** Jul 2022 – 2023  
**Team Size:** ~6 members  
**My Position in Team:** Team Lead  
**One-line Summary:** Built a machine learning classification project to predict whether a patient would miss a medical appointment, using a Kaggle healthcare dataset to learn and demonstrate the end-to-end ML workflow.

---

## 1. Problem / Why It Existed

### Business Problem

Patient no-shows can result in unused appointment slots and reduce scheduling efficiency. Predicting whether a patient is likely to miss an appointment can potentially help healthcare organizations make better scheduling and reminder decisions.

### Technical Problem

This project was **not a production/client healthcare solution**. It was a structured ML learning project assigned to employees who were on the Capgemini bench.

The mentor provided the Kaggle **Medical Appointment No Shows** dataset and guided the team through the machine learning workflow:

```text
Understand the data
      ↓
EDA
      ↓
Data cleaning
      ↓
Feature engineering
      ↓
Data encoding
      ↓
Train multiple ML models
      ↓
Compare model results
      ↓
Select the better-performing model
      ↓
Present the results
```

The main objective was to understand practical machine learning fundamentals and how to take a dataset through an end-to-end classification workflow.

### Who Used It

This was an internal learning/upskilling project.

There was no production end user and the model was not deployed into a live scheduling system.

### Why This Solution Was Needed

The project gave the team hands-on experience with:

- Healthcare-style tabular data.
- Exploratory data analysis.
- Data cleaning.
- Feature engineering.
- Categorical encoding.
- Classification algorithms.
- Model evaluation and comparison.
- Basic model selection.

---

## 2. My Role & Ownership

### What I Personally Built

I was selected by the mentor as the **team lead**.

My responsibilities included:

- Working on the ML data-analysis and modeling workflow.
- Understanding and implementing the data preparation and feature-engineering concepts taught by the mentor.
- Participating in model experimentation and comparison.
- Consolidating the team's work into the final Jupyter Notebook/report.
- Preparing the final presentation/PPT.
- Presenting the project to the mentor.

### Team Leadership

The team had approximately **6 members including me**.

I was responsible for:

- Coordinating team meetings.
- Leading the team's Scrum-style coordination activities.
- Assigning team members different ML models to learn and implement.
- Asking team members to explain their assigned models to the rest of the team.
- Coordinating the comparison of the model results.
- Bringing the individual pieces together into the final deliverable.

### What Other Team Members Owned

The team members worked on different ML models and shared their understanding/results with the group.

The exact ownership of each individual model is not fully recalled.

---

## 3. System / Product Overview

This was a machine learning notebook-based project rather than a deployed application.

### What the System Does

The project takes historical patient appointment data and prepares it for a binary classification task:

```text
Patient + Appointment Information
             ↓
       Data Cleaning
             ↓
      Feature Engineering
             ↓
      Categorical Encoding
             ↓
         EDA / Analysis
             ↓
       Train ML Models
             ↓
      Evaluate & Compare
             ↓
       Select Best Model
```

The target represented whether the patient showed up for the appointment or did not show up.

### Dataset

The mentor provided the Kaggle **Medical Appointment No Shows** dataset.

The dataset contained approximately **110,000 appointment records** from Brazil covering appointments from around November 2015 to June 2016.

---

## 4. Architecture / How It Worked

Since this was an ML learning project, the architecture was primarily a data-processing and modeling pipeline.

### Step-by-Step Flow

#### Step 1 — Load the Dataset

The dataset was loaded into Python using Pandas.

Basic dataset inspection included:

- Number of rows.
- Number of columns.
- Column names.
- Data types.
- Null/missing values.
- Basic descriptive statistics.
- Mean, median and mode where appropriate.

I initially learned much of this basic EDA workflow through a Medium article and implemented it in the project.

#### Step 2 — Understand the Data

The team identified:

- Numerical features.
- Categorical features.
- Date/time fields.
- Target variable.
- Patient and appointment identifiers.

#### Step 3 — Exploratory Data Analysis

The team analyzed the distribution of the target and relationships with different patient/appointment attributes.

EDA included visualizations such as:

- Count plots.
- Box plots.
- Correlation heatmaps.
- Age-based analysis.
- Show/no-show comparisons.

The mentor guided the team on what EDA means, why it is performed, and how to interpret the results.

### EDA Observations I Remember

#### SMS Reminders

The analysis suggested that appointment reminders were related to attendance behavior.

My understanding from the analysis was that reminding patients about their appointment could help reduce no-shows.

#### Age

Age groups showed different no-show behavior.

I specifically remember observing:

- Lower no-show behavior among infants.
- Higher no-show behavior in the approximately 20–30 age range.

#### Gender

Gender did not show a major difference that I remember from the analysis.

#### Other Features

The exact findings for:

- Scholarship
- Neighbourhood

are not recalled and should not be presented as confirmed findings.

---

## 5. Data Cleaning & Feature Engineering

### Date Features

The dataset contained appointment scheduling and appointment date information.

The mentor explained that the difference between the scheduling date and actual appointment date could potentially provide useful information for prediction.

The project extracted:

- Day.
- Month.
- Year initially.
- Day of week.

The year was later dropped because it was effectively constant in the dataset.

### DaysBetween

A feature was created representing the number of days between:

```text
Appointment Date - Scheduled Date
```

This represented the waiting period between scheduling the appointment and the actual appointment.

The reasoning was that the amount of time between scheduling and the appointment could potentially influence whether the patient eventually attended.

I understood the reasoning explained by the mentor and implemented the feature accordingly.

### Invalid Date Records

The date-derived analysis revealed records with logically invalid date relationships.

Approximately five records had a negative date difference.

These records were treated as incorrect data and removed.

### Patient / Appointment Identifiers

Identifiers such as:

- `PatientId`
- `AppointmentID`

were not useful predictive features and were excluded from the modeling data.

### Age Data

During EDA, the age visualization showed records with `Age = 0`.

Initially, this appeared unusual.

The mentor explained that these could represent infants, so these records were not automatically removed.

The project therefore retained legitimate `Age = 0` records.

### Age = -1

An invalid negative age value was also encountered.

The exact handling of the `Age = -1` record(s) is **not fully recalled** and should be verified from the original notebook before being described more specifically.

---

## 6. Categorical Encoding

Machine learning models required numerical representations of the categorical values used in the training data.

### Binary Values

Binary categorical values such as:

```text
Yes → 1
No  → 0
```

were converted into numerical representations.

For example, the `No-show` target was represented numerically for modeling.

### Gender

Gender values were also converted into numerical representation.

### Neighbourhood

`Neighbourhood` contained text categories.

The mentor explained that one-hot encoding could create a large number of additional columns because there were many neighbourhood categories.

For this project, the team therefore used **label encoding**, assigning numerical labels to the neighbourhood categories.

The exact sklearn implementation/class used for this encoding is not currently recalled.

---

## 7. Tech Stack

| Technology | Where It Was Used | Why It Was Used |
|---|---|---|
| **Python** | Overall ML workflow | Primary programming language |
| **Pandas** | Data loading and manipulation | Working with tabular healthcare data |
| **NumPy** | Numerical operations | Supporting data processing |
| **Matplotlib** | Visualization | Creating EDA visualizations |
| **Seaborn** | Visualization | Creating statistical plots and correlation heatmaps |
| **Scikit-learn** | ML workflow | Data preparation, model training/evaluation and ML utilities |
| **XGBoost** | Classification experimentation | Compare gradient-boosting performance |
| **CatBoost** | Classification experimentation | Compare another gradient-boosting approach; ultimately selected based on results |

---

## 8. Machine Learning / Model Comparison

The team experimented with multiple classification approaches.

Different team members were assigned different models to learn and implement.

The exact complete list of models in the final comparison is **not fully recalled**.

The team compared the model results rather than selecting a single algorithm without experimentation.

### XGBoost and CatBoost

XGBoost and CatBoost were specifically suggested by the mentor.

After comparing the results, these two models were relatively close.

CatBoost achieved the higher accuracy, and the team selected CatBoost as the final model.

Other evaluation metrics such as precision, recall and F1-score were also considered, although the exact metric-by-metric comparison is not currently recalled.

---

## 9. Key Technical Decisions

### Decision 1 — Compare Multiple Models

**What:** Compare multiple classification algorithms.

**Why:** The objective was to understand how different ML algorithms performed on the same dataset rather than assuming one algorithm would be best.

**Who influenced the decision:** The mentor guided the team toward model comparison.

**Result:** The team could compare the models based on their observed performance.

---

### Decision 2 — Create `DaysBetween`

**What:** Calculate the number of days between scheduling and the appointment.

**Why:** The mentor suggested that the waiting period could contain predictive information about whether a patient would show up.

**My contribution:** I understood the reasoning and implemented the feature.

---

### Decision 3 — Label Encoding for Neighbourhood

**What:** Convert neighbourhood categories into numerical labels.

**Why:** The mentor explained that one-hot encoding would create many additional columns because of the number of neighbourhood categories.

**Trade-off:** Label encoding reduced dimensionality but assigned numerical labels to categories.

---

### Decision 4 — Select CatBoost

**What:** Select CatBoost after comparing multiple models.

**Why:** CatBoost achieved the higher accuracy among the closely performing models, particularly compared with XGBoost.

**Decision ownership:** This was a team decision based on the observed model results.

---

## 10. Challenges & How I Solved Them

### Challenge 1 — Understanding Raw Healthcare Data

**Problem:** The dataset contained many columns with different types of information.

**Solution:** Performed basic EDA to understand rows, columns, data types, missing values and statistical properties.

The mentor guided the team through how to interpret the data.

---

### Challenge 2 — Understanding Feature Engineering

**Problem:** Raw date fields did not directly express the potentially useful waiting period between scheduling and appointment.

**Solution:** With mentor guidance, created date-derived features and a `DaysBetween` feature.

---

### Challenge 3 — Unusual Age Values

**Problem:** The age visualization showed `Age = 0`.

**Initial concern:** A zero age appeared unusual.

**Solution:** The mentor explained that these could represent infants. The records were therefore retained instead of being blindly removed.

---

### Challenge 4 — Invalid Data

**Problem:** Some appointment records produced negative date differences.

**Solution:** The records were identified as logically invalid and removed.

---

### Challenge 5 — Learning Multiple Models as a Team

**Problem:** The team needed to understand different ML algorithms rather than simply use one model.

**Solution:** I divided model-learning responsibilities among team members. Each member learned a model and explained it to the rest of the team.

This allowed the team to collectively understand and compare multiple approaches.

---

## 11. Testing / Validation

The project used a train/test split and compared model performance using classification evaluation metrics.

The evaluation included:

- Accuracy.
- Precision.
- Recall.
- F1-score.
- Confusion matrix.

The exact per-class metric values are not currently recalled.

### Hyperparameter Tuning

The original project documentation indicates that CatBoost was further tuned using `GridSearchCV`.

However, I do **not currently remember the details of the tuning process well enough to confidently explain:

- Why the selected cross-validation configuration was used.
- The complete parameter search space.
- Whether I personally implemented the tuning or another team member did.
- The exact final configuration.

These details should therefore be verified from the original notebook before being used as detailed interview claims.

---

## 12. Production / Deployment

This project was **not deployed to production**.

It remained an internal learning/analysis project based on a public Kaggle dataset.

There was:

- No production API.
- No live scheduling-system integration.
- No production model serving.
- No automated retraining pipeline.

The final deliverables were primarily the Jupyter Notebook/report and presentation.

---

## 13. Impact / Results

### Technical Impact

The project provided hands-on experience with the complete ML classification workflow:

```text
Raw Data
   ↓
Data Understanding
   ↓
EDA
   ↓
Data Cleaning
   ↓
Feature Engineering
   ↓
Categorical Encoding
   ↓
Model Training
   ↓
Model Comparison
   ↓
Model Selection
```

### Team Impact

As team lead, I:

- Coordinated a team of approximately six members.
- Distributed model-learning responsibilities.
- Organized team meetings.
- Helped the team share understanding of different ML models.
- Consolidated the final technical work.
- Prepared the final Jupyter Notebook/report.
- Prepared and presented the final PPT to the mentor.

### Model Result

CatBoost emerged as the selected model after comparison with the other approaches.

The existing project notes report a tuned accuracy of approximately **79.88%**, but the exact hyperparameter-tuning process and configuration should be verified from the original notebook before treating those details as interview-ready facts.

### Business Impact

There was **no measured business impact**, because this was not deployed to a live healthcare scheduling environment.

The primary outcome was successful completion of the ML learning exercise and practical experience with classification modeling.

---

## 14. Resume / Portfolio Summary

### Short Summary

Built an end-to-end patient no-show classification project using a Kaggle healthcare dataset as part of a Capgemini ML learning initiative. Led a ~6-member team, coordinated model experimentation, implemented data cleaning and feature engineering, and consolidated the final Jupyter Notebook and presentation. Compared multiple classification approaches and selected CatBoost based on model performance.

### Resume-Oriented Bullets

- Led a ~6-member team in building an end-to-end **patient no-show prediction** classification project using Python, Pandas, Scikit-learn, XGBoost, and CatBoost.
- Implemented data cleaning, EDA, categorical encoding, and date-based feature engineering, including a `DaysBetween` feature representing appointment waiting time.
- Coordinated multi-model experimentation and helped consolidate model results, with **CatBoost selected as the best-performing approach based primarily on accuracy**.
- Prepared the final Jupyter Notebook/report and presentation, and presented the solution to the project mentor.

---

## 15. Interview Talking Points

### 1. End-to-End ML Workflow

> "This was one of my first hands-on ML projects at Capgemini. I worked through the complete workflow from understanding raw data and EDA to feature engineering, model training, evaluation and model comparison."

### 2. Team Leadership + Technical Contribution

> "I was selected by the mentor as the team lead for a six-member team. I coordinated the meetings, divided model-learning responsibilities, helped the team share their understanding, and consolidated the final notebook and presentation."

### 3. Data Quality and Feature Engineering

> "One thing I learned was not to blindly remove unusual data. For example, I initially noticed age-zero records, but my mentor explained these could represent infants. We also created a `DaysBetween` feature because the waiting period between scheduling and the appointment could potentially influence no-show behavior."

---

## 16. Likely Interview Questions

### Q1. Was this a production project?

**Answer:**  
No. It was an internal Capgemini bench-learning/upskilling project using a mentor-provided Kaggle dataset. It was not deployed into a live healthcare scheduling system.

### Q2. What was your role?

**Answer:**  
I was selected as the team lead. I coordinated approximately six team members, managed meetings and Scrum-style coordination, assigned different models for team members to learn, consolidated the final notebook/report and prepared the final presentation.

### Q3. Why did you create `DaysBetween`?

**Answer:**  
The mentor explained that the waiting period between scheduling an appointment and the actual appointment could potentially affect whether a patient attends. I implemented that as a feature representing the number of days between the two dates.

### Q4. Why did you keep `Age = 0`?

**Answer:**  
I noticed the zero values during EDA. My mentor explained that these could represent infants, so we didn't automatically treat them as invalid data and remove them.

### Q5. Why did you compare multiple models?

**Answer:**  
The purpose was to understand and compare different classification algorithms rather than assuming one model would work best. Different team members worked on different models, and we compared their results as a team.

### Q6. Why did you select CatBoost?

**Answer:**  
CatBoost and XGBoost were relatively close, but CatBoost achieved the higher accuracy. We also considered other classification metrics, and the team selected CatBoost based on the overall observed performance.

### Q7. Did you deploy the model?

**Answer:**  
No. This was an internal learning/prototyping project and remained in the notebook/report stage.

### Q8. What was the biggest thing you learned?

**Answer:**  
I learned how the pieces of an ML project connect end-to-end: understanding the data, performing EDA, cleaning and engineering features, encoding categorical data, comparing models, interpreting evaluation results, and selecting a model based on evidence.

---

## 17. Open Questions / Gaps

- [ ] Verify the **exact complete list of ML models** used in the final project.
- [ ] Verify the exact implementation/class used for **Neighbourhood label encoding**.
- [ ] Verify the exact handling of **`Age = -1`**.
- [ ] Verify the exact per-model **accuracy, precision, recall and F1-score**.
- [ ] Verify whether `GridSearchCV` was personally implemented by me or by another team member.
- [ ] Verify the exact **cross-validation configuration** used for CatBoost.
- [ ] Verify the exact CatBoost hyperparameters from the original notebook before using them as interview claims.
- [ ] Verify the reported **79.88% accuracy** from the original notebook.
- [ ] Verify the exact team size if the original project records are available.
- [ ] Verify the exact Scrum terminology/process used by the team before describing it as formal Scrum.

---

## 18. Personal Learning / Takeaways

- Learned the practical workflow of a supervised ML classification project.
- Learned how to perform basic EDA and understand the structure and quality of a dataset.
- Learned that feature engineering can transform raw fields into information that may be more useful for a model.
- Learned to investigate unusual data rather than automatically removing it.
- Learned the basic differences between several classification approaches through team-based experimentation.
- Learned the importance of comparing model performance rather than selecting a model arbitrarily.
- Developed early experience in **technical team leadership**, knowledge sharing, coordination, and consolidating work from multiple contributors.
- Built confidence in presenting a technical ML project through the final Jupyter Notebook and PPT presentation.
