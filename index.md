## Welcome to MIMIC TBI Machine Learning Test Codes!

### Traumatic Brain Injury (TBI) Introduction
Worldwide, in 2016, there were approximately 27 million new cases of TBI with an age-adjusted incidence rate of 369 per 100,000—representing a 3.6% increase from 1990. In the same year, prevalence was 55.5 million individuals, representing an 8.4% increase from 1990 (Global Burden of Disease [GBD], 2019)

### Objective of this test code
The code tries to accomplish three tasks:

1. Connect MIMIC database (local postgres SQL instance) and Run SQL from jupyter notebook to query a mTBI table from relevant clinic data. This requires clinical information about criteria. Please refer to attached TBI paper for Glascow Coma Score (GCS) criteria and ICD query selection.
2. Visualize the data and remove outliers or better machine learning performance
3. Predict ICU survival (motality) rate using age, gender, GCS score and Delay time between admission and chart event (chartdelayhrs). Random forest was used.
    
### Findings
Overall AUC of 0.89 was achieved. Most important factors are delay and age. 

=== Model Score ===
89.97

### MIMIC Database
MIMIC is an openly available dataset developed by the MIT Lab for Computational Physiology, comprising deidentified health data associated with ~60,000 intensive care unit admissions. It includes demographics, vital signs, laboratory tests, medications, and more. See more about MIMIC here: https://mimic.physionet.org/about/mimic/

### Limitations
Because MIMIC database only includes ICU EMR data, the code has limitations:

1. prediction is more needed in ER stage, ideally leveraging point of care biomakers to have instant results. Patient got admit by ICU after triage of ER. So the uncertainty is less than ER patient.
2. no connection with real world ER data yet. After connected and trained using RWD, ML models may play a role of predicting or triaging patient for mTBI.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
