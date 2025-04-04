# 🧬 COVID-19 CBC Dataset Metadata
---

## About Dataset
### **COVID-19 Complete Blood Count (CBC) Database**
A team of researchers and doctors from Qatar University, Doha, Qatar, and Dhaka Medical College Hospital, Bangladesh, have created a database of complete blood count, demographic data, and corresponding patients' outcome. The data was collected between 12 April and 31 August 2020 at Dhaka Medical College Hospital, Bangladesh which is approved by the Hospital Ethical Committee. Clinical parameters with hospital admission, discharge/death outcomes were collected for 103 patients (Survived-61 (59.22%), Death-42 (40.78%)).

**Objective**
Researchers can use this database to produce useful and impactful scholarly work on COVID-19, which can help in tackling this issue.

##  Patient Information

| Column Name              | Type     | Description                                                   | Relevance                         |
|--------------------------|----------|---------------------------------------------------------------|-----------------------------------|
| `Admission_DATE`         | Date     | Date of hospital admission                                     | Used to calculate length of stay |
| `Discharge_DATE` / `date of Death` | Date | Date of discharge or death                                     | Final status determination        |
| `Outcome`                | Categorical (Survived/Death) | Patient outcome (target variable)                              |   Target variable                |
| `Patient Age`            | Numeric  | Patient's age in years                                         | Risk increases with age           |
| `Gender`                 | Categorical (M/F) | Biological sex                                                 | Males may show higher severity    |
| `Sample Collection Date`| Date     | Date CBC sample was taken                                      | Helps track timeline              |
| `Treatment Provided`     | Text     | Description of treatment approach                              | Can suggest intervention level    |
| `Ventilated`             | Categorical (Y/N) | Whether the patient was on ventilation                        | Proxy for critical condition      |

---

## Complete Blood Count (CBC) Parameters

| Column Name                   | Type     | Description                                                        | Biological Relevance                           |
|-------------------------------|----------|--------------------------------------------------------------------|-------------------------------------------------|
| `Red blood cell distribution width (RDW)` | Numeric  | Measures variation in red blood cell size                          | High RDW may indicate inflammation, mortality   |
| `Monocytes (%)`               | Numeric  | Percentage of monocytes in white blood cells                       | Changes in monocyte count affect immune response |
| `White blood cell count`      | Numeric  | Total WBCs per microliter                                          | High/low counts indicate infection severity     |
| `Platelet Count`              | Numeric  | Platelets per microliter of blood                                  | Low platelets (thrombocytopenia) = higher risk  |
| `Lymphocyte Count`            | Numeric  | Number of lymphocytes (key immune cells)                           | Low lymphocytes (lymphopenia) = bad prognosis   |
| `Neutrophils Count`           | Numeric  | Number of neutrophils (inflammatory cells)                         | High neutrophils = cytokine storm, severe cases |

---

## Notes for Modeling

- **Missing Values**: Some clinical parameters may be missing—handle with imputation or deletion.
- **Imbalance**: Dataset is imbalanced (Survived: ~59%, Death: ~41%) — use SMOTE or class weights.
- **Date Columns**: Useful for deriving duration-based features like Length of Stay.

---
## 📚 Dataset Reference

This dataset was collected by researchers from **Qatar University** and **Dhaka Medical College Hospital**.

🗂️ **Dataset Source**:  
[COVID-19 Complete Blood Count (CBC) Database](https://www.kaggle.com/datasets/tawsifurrahman/covid19-complete-blood-count-clinical-database)