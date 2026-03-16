# Skiing and Snowboarding Injury Analysis

Machine learning analysis of skiing and snowboarding injuries using the **National Electronic Injury Surveillance System (NEISS)** dataset from **2016–2024**.

This project analyzes injury patterns among winter sports participants in the United States and builds predictive models to examine how injury characteristics changed over time. The analysis combines exploratory data analysis, feature engineering, and machine learning models to identify patterns associated with injury outcomes.

---

# Project Motivation

Skiing and snowboarding are among the most popular winter recreational activities in the United States. While participation continues to grow, these sports also present a meaningful risk of injury. Understanding how injury patterns vary across demographic groups, injury types, and time periods can provide insight for injury prevention strategies and healthcare resource planning.

The goal of this project was to:

• Explore injury patterns among skiing and snowboarding participants
• Examine whether injury characteristics changed over time
• Build machine learning models to classify injuries into pre- and post-pandemic periods
• Evaluate model performance and interpret important predictors of injury patterns

---

# Dataset

**Source:**
U.S. Consumer Product Safety Commission — National Electronic Injury Surveillance System (NEISS)

**Description:**
NEISS is a nationally representative injury surveillance database that collects injury reports from approximately 100 emergency departments across the United States.

Each record represents a consumer-product–related injury treated in an emergency department.

**Time range used:**
2016–2024

**Population represented:**
Patients presenting to U.S. emergency departments with injuries related to skiing or snowboarding.

---

# Key Variables

| Variable    | Description                 |
| ----------- | --------------------------- |
| Age         | Age of injured patient      |
| Sex         | Patient sex                 |
| Sport       | Skiing or snowboarding      |
| Diagnosis   | NEISS injury diagnosis code |
| Body_Part   | Body region injured         |
| Disposition | Outcome after ED visit      |
| Year        | Year of injury              |

---

# Data Preparation

The dataset required several preprocessing steps prior to modeling:

• Filtering records for skiing and snowboarding product codes
• Cleaning categorical variables and resolving coding inconsistencies
• Handling missing values
• Creating age group features
• Encoding categorical variables using one-hot encoding
• Splitting the dataset into training and testing subsets

A preprocessing pipeline was implemented using **Scikit-Learn’s ColumnTransformer** to ensure consistent feature processing across models.

---

# Modeling Approach

Two classification models were evaluated:

### Logistic Regression (Baseline)

Used as an interpretable baseline model to establish expected classification performance.

### Random Forest Classifier

A non-linear ensemble model used to capture more complex relationships between injury characteristics and time period classification.

The modeling pipeline included:

• Feature preprocessing
• Train-test split
• Model training
• Model evaluation using multiple metrics

---

# Model Evaluation

Model performance was evaluated using:

• Accuracy
• Precision
• Recall
• F1-Score
• ROC-AUC
• Confusion Matrix

The Random Forest model demonstrated improved predictive performance relative to the baseline logistic regression model.

---

# Example Model Outputs

## Example Model Outputs

### ROC Curve
![ROC Curve](figures/roc_curve.png)

### Random Forest Confusion Matrix
![Confusion Matrix](figures/confusion_matrix_rf.png)

### Feature Importance
![Feature Importance](figures/feature_importance.png)

Feature importance analysis highlights which injury characteristics most strongly contributed to classification performance.

---

# Key Findings

• Injury patterns differed between skiing and snowboarding participants
• Upper extremity injuries were more common among snowboarders
• Lower extremity injuries were more prevalent among skiers
• Machine learning models were able to identify meaningful structure in injury characteristics across time periods

These results illustrate how injury surveillance data can be used to better understand sports injury trends.

---

# Project Structure

```
ski-snowboard-injury-analysis
│
├── notebooks
│   ├── M2_Data_EDA_report.ipynb
│   ├── M3_Model_Evaluations.ipynb
│   └── M4_Final_Deliverables.ipynb
│
├── figures
│   ├── roc_curve.png
│   ├── confusion_matrix_rf.png
│   └── feature_importance.png
│
├── report
│   └── project_report.pdf
│
├── presentation
│   └── project_slides.pdf
│
└── README.md
```

---

# Tools and Libraries

Python
Pandas
NumPy
Scikit-Learn
Matplotlib
Seaborn
Jupyter Notebook

---

# Limitations

• NEISS captures only injuries treated in emergency departments
• Injuries treated at urgent care or outside healthcare systems are not included
• Limited clinical detail regarding injury severity
• Observational cross-sectional data limits causal interpretation

---

# Ethical Considerations

The dataset is fully de-identified and publicly available through the U.S. Consumer Product Safety Commission. Results are interpreted as descriptive associations rather than causal conclusions.

---

# Future Work

Future work could expand this analysis by:

• Incorporating additional injury surveillance datasets
• Modeling injury severity outcomes
• Investigating geographic variation in injury patterns
• Applying temporal modeling approaches to examine injury trends over time

---

# Author

Freddy Chavez
MS Data Science — California State University Northridge
