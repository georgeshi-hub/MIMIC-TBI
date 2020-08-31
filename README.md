# MIMIC-TBI-survival

Traumatic Brain Injury (TBI) is a deadly disease that often cause deaths. And mile TBI (mTBI) is often neglected due to lack of symtoms.

The code tries to accomplish three tasks:
1. connect MIMIC database (local postgres instance).  See more about MIMIC here: https://mimic.physionet.org/about/mimic/
2. run SQL from jupyter notebook to query a mTBI table from relevant clinic data. This requires clinical information about criteria. Please refer to attached TBI paper for GCS criteria and ICD query selection. 
3. predict ICU survival (motality) rate using data such as CT and GCS score. various models are used and compared. 

Because MIMIC database only includes ICU EMR data, the code has limitations: 
1. prediction is more needed in ER stage, ideally leveraging point of care biomakers to have instant results. Patient got admit by ICU after triage of ER. So the uncertainty is less than ER patient.
2. no connection with real world ER data yet. After connected and trained using RWD, ML models may play a role of predicting or triaging patient for mTBI.

