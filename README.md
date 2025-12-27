# 💊 Prescription Fraud Detection – Data Analytics & Preprocessing Project

This project performs complete **data exploration, preprocessing, fraud trend analysis, statistical analysis, aggregation, visualization, and feature preparation** on a prescription dataset.  
It prepares the dataset so that machine learning models can later be built to detect fraudulent prescription claims.

---

## 🎯 Project Objective

The goal of this project is to:

- Understand and analyze prescription data
- Detect hidden fraud patterns and suspicious behavior
- Clean and prepare dataset for machine learning
- Perform statistical analysis on prescription cost
- Examine seasonal/monthly trends of fraudulent claims
- Encode and scale data for ML-readiness
- Convert raw categorical and text-based fields into numerical ML features

---

## 📂 Dataset Description

The dataset contains **500 rows × 25 columns**.  
Below are the types of information available in the dataset:

| Field | Meaning |
|-------|---------|
| Prescription_ID | Unique identifier for each prescription |
| Patient_ID | Unique identifier assigned to each patient |
| Doctor_ID | Unique identifier of prescribing doctor |
| Pharmacy_ID | Unique pharmacy identifier |
| Drug_Name | Name of prescribed medication |
| Drug_Category | Type/category of drug (e.g., Antibiotic, Hypertension) |
| Dosage | Contains numeric + string format (e.g., "98mg") |
| Prescription_Date | Date when prescription was issued |
| Prescription_Filled_Date | Date when medication was dispensed |
| Insurance_Claim | Binary field (0 = not claimed, 1 = claimed) |
| Total_Cost | Total dollar cost of prescription |
| Refill_Count | Number of refill requests |
| Patient_Age | Age of patient |
| Patient_Gender | Gender |
| Patient_Health_Condition | Medical condition of patient |
| Prescription_Status | Whether filled, canceled, pending |
| Drug_Schedule | Regulatory classification (Schedule II, III, etc.) |
| Patient_Region | Geographic region of patient |
| Doctor_Region | Region where doctor practices |
| Pharmacy_Region | Pharmacy location |
| Doctor_Flagged | 0 or 1 — whether doctor is marked suspicious |
| **Fraudulent_Claim** | 🎯 Target variable – whether this prescription is fraudulent (0 = No, 1 = Yes) |

---

## 🧹 Data Preprocessing Details

The following data-cleaning and preprocessing techniques were applied:

### 1️⃣ Cleaning Data and Converting Text Fields
```python
df['Dosage'] = df['Dosage'].apply(lambda x: int(x[:-2]))


