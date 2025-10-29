# CODEBOOK – Obesity Levels Estimation Dataset

**Source:**  
UC Irvine Machine Learning Repository – [Estimation of obesity levels based on eating habits and physical condition](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition)  
Original publication: F. Mendoza Palechor & A. de la Hoz Manotas (2019). *Dataset for estimation of obesity levels based on eating habits and physical condition in individuals from Colombia, Peru and Mexico.*  
[DOI: 10.1016/j.dib.2019.104344](https://doi.org/10.1016/j.dib.2019.104344)

---

## General Information

- **Population:** Individuals aged 14–61 from **Mexico, Peru, and Colombia**.  
- **Collection method:** Online survey over 30 days.  
- **Attributes:** 17 predictors + 1 target variable (`NObesity`).  
- **Sample size:** 2,111 records.  
- **Balancing method:** 77% synthetic data created using **SMOTE**; 23% original survey responses.  
- **Purpose:** To analyze how eating habits and physical condition relate to obesity levels and enable predictive modeling.  

Each observation represents **one respondent**, and each variable below corresponds to a survey question or calculated field.

---

## Variable Descriptions

| Variable | Type | Description / Question | Possible Values or Units |
|-----------|------|------------------------|---------------------------|
| **Gender** | Categorical | Biological sex of the respondent. | `Female`, `Male` |
| **Age** | Numeric | Age in years. | 14–61 |
| **Height** | Numeric | Height of the individual. | Meters (m) |
| **Weight** | Numeric | Weight of the individual. | Kilograms (kg) |
| **family_history_with_overweight** | Categorical | “Has a family member suffered or currently suffers from overweight?” | `Yes`, `No` |
| **FAVC** | Categorical | “Do you eat high-caloric food frequently?” | `Yes`, `No` |
| **FCVC** | Ordered Factor | “How often do you eat vegetables in your meals?” | `Never` (1), `Sometimes` (2), `Always` (3) |
| **NCP** | Ordered Factor | “How many main meals do you have daily?” | `1–2`, `3`, `More_than_3` |
| **CAEC** | Ordered Factor | “Do you eat food between meals (snacks)?” | `No`, `Sometimes`, `Frequently`, `Always` |
| **CH2O** | Ordered Factor | “How much water do you drink daily?” | `<1L`, `1–2L`, `>2L` |
| **CALC** | Ordered Factor | “How often do you drink alcohol?” | `I_do_not_drink`, `Sometimes`, `Frequently`, `Always` |
| **SCC** | Categorical | “Do you monitor your daily calorie intake?” | `Yes`, `No` |
| **FAF** | Ordered Factor | “How often do you engage in physical activity?” | `None`, `1–2_days`, `2–4_days`, `4–5_days` |
| **TUE** | Ordered Factor | “How much time do you use technology devices daily?” | `0–2_hours`, `3–5_hours`, `>5_hours` |
| **SMOKE** | Categorical | “Do you smoke?” | `Yes`, `No` |
| **MTRANS** | Categorical | “What type of transportation do you use most frequently?” | `Automobile`, `Motorbike`, `Bike`, `Public_Transportation`, `Walking` |
| **NObesity** *(Target)* | Ordered Factor | Obesity level category calculated from BMI (WHO & Mexican Normativity). | `Insufficient_Weight`, `Normal_Weight`, `Overweight_Level_I`, `Overweight_Level_II`, `Obesity_Type_I`, `Obesity_Type_II`, `Obesity_Type_III` |

---

## Derived Variables

- **BMI (Body Mass Index)** = `Weight / (Height^2)`  
  Used to determine the `NObesity` category based on WHO/Mexican thresholds:  
  - *Underweight:* < 18.5  
  - *Normal:* 18.5–24.9  
  - *Overweight I:* 25–29.9  
  - *Overweight II:* 30–34.9  
  - *Obesity I:* 35–39.9  
  - *Obesity II:* 40+  

*(BMI itself is not included as a separate variable, but derived internally to label obesity categories.)*

---

## Data Quality Notes

- **Synthetic balancing:** SMOTE generated minority class samples to ensure evenly distributed classes across seven obesity levels.  
- **Data cleaning:** Outliers and missing values were removed before applying SMOTE.  
- **Normalization:** Continuous features (age, height, weight) were standardized before model use.  
- **Limitation:** Because 77% of data is synthetic, correlations and inferences should be interpreted with caution.

---

## References

Palechor, F. M., & Manotas, A. H. (2019). *Dataset for estimation of obesity levels based on eating habits and physical condition in individuals from Colombia, Peru and Mexico.*  
**Data in Brief, Volume 25**, 104344.  
[https://doi.org/10.1016/j.dib.2019.104344](https://doi.org/10.1016/j.dib.2019.104344)

---
