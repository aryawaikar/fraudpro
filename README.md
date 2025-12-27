# 💊 Prescription Fraud Detection – Data Analytics & Preprocessing Project

This project performs **data exploration, preprocessing, statistical analysis, fraud trend analysis, aggregation, and visualization** to understand and prepare medical prescription data for a downstream fraud-detection model.

---

## 🎯 Project Objective

- Analyze prescription dataset for fraud signals
- Clean raw data & make it ML-ready
- Perform statistics on prescription cost
- Visualize fraud behavior trends
- Identify anomaly patterns (cost, refill, flagged doctors)
- Encode & scale features for model-training

---

## 📂 Dataset Summary

Dataset Shape: **500 rows × 25 columns**  
Extracted from notebook: :contentReference[oaicite:1]{index=1}

| Column Example | Description |
|----------------|-------------|
| Prescription_ID | Unique record identifier |
| Patient_ID / Doctor_ID / Pharmacy_ID | Entity identifiers |
| Drug_Name / Drug_Category | Medication details |
| Dosage | e.g., `"98mg"` → converted into integer `98` |
| Prescription_Date / Filled_Date | Timeline of prescription lifecycle |
| Insurance_Claim | 0 = not claimed, 1 = claimed |
| Total_Cost | Medication financial value |
| Refill_Count | Times prescription was refilled |
| Doctor_Specialty / Patient_Health_Condition | Medical metadata |
| Patient_Region / Doctor_Region / Pharmacy_Region | Geographic patterns |
| Doctor_Flagged | Doctor suspicious-behaviour flag |
| **Fraudulent_Claim** | 🎯 Target variable (0 = normal / 1 = fraud) |

---

## 🧹 Data Preprocessing Steps

Performed operations include:  
:contentReference[oaicite:2]{index=2}

✔ Type conversion (`98mg` → `98`)  
✔ Missing value handling using `SimpleImputer`  
✔ One-Hot Encoding for categorical columns  
✔ Scaling numerical fields (`Total_Cost`, `Dosage`, `Patient_Age`, `Days_Supply`)  
✔ Output dataset expanded to **132 ML-ready columns**

