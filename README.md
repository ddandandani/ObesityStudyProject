# ObesityStudyProject
DS-310 Course Project

# Obesity Levels Estimation Dataset

**Source:**  
UC Irvine Machine Learning Repository – [Estimation of obesity levels based on eating habits and physical condition](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition)  
**Original Article (Data in Brief, Elsevier):**  
F. Mendoza Palechor & A. de la Hoz Manotas (2019). *Dataset for estimation of obesity levels based on eating habits and physical condition in individuals from Colombia, Peru and Mexico.*  
[DOI: 10.1016/j.dib.2019.104344](https://doi.org/10.1016/j.dib.2019.104344)  

**License:** Creative Commons BY 4.0 (Free to use with attribution)

---

## Description
This dataset contains information used to estimate **obesity levels** of individuals from **Mexico, Peru, and Colombia**, based on self-reported **eating habits** and **physical condition** collected through an online survey.  
It includes **2,111 records** and **17 attributes** describing dietary patterns, hydration, physical activity, technology use, and basic demographics. Each record is labeled with the target variable **`NObesity`**, which classifies participants into one of seven categories:

`Insufficient_Weight`, `Normal_Weight`, `Overweight_Level_I`, `Overweight_Level_II`, `Obesity_Type_I`, `Obesity_Type_II`, `Obesity_Type_III`.

---

## Dimensions
| Description | Count |
| Observations (rows) | 2,111 |
| Variables (columns) | 18 (17 predictors + 1 outcome) |

---

## What each row represents
Each row corresponds to a **single survey respondent**, aged **14 – 61**, who answered questions about their lifestyle (food, exercise, hydration, technology use, and transportation). Physical variables such as height and weight were used to compute BMI and assign the obesity level according to **WHO and Mexican Normativity** standards.

---

## Data Collection and Processing
- Data were gathered through a **30-day online survey** hosted in Mexico, Peru, and Colombia.  
- Responses were **cleaned**, normalized, and balanced using **SMOTE** (Synthetic Minority Over-sampling Technique) in Weka.  
  - **77 %** of records are synthetic (for class balancing).  
  - **23 %** are original survey responses.  
- Attributes were chosen through a **literature review** on nutrition and physical activity factors linked to obesity.  
- All records were labeled according to BMI-based thresholds.  
- The dataset is suitable for **classification, prediction, segmentation, and association analyses**.

---

## File List
| File | Description |
| `obesity.csv` | Main dataset in CSV format |
| `CODEBOOK.md` | Detailed variable definitions and value levels |
| `README.md` | This summary file |

---

## Notes
- All analyses for this project will be performed in **RStudio** using the data provided here.  
- For variable definitions and units, refer to the accompanying **`CODEBOOK.md`** file.  
- When citing this dataset, please include the DOI above.

---
