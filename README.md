# Death and Dialysis

_A data science exploration of how transfusion rates relate to mortality in U.S. dialysis facilities._

---

## Introduction

Each day, thousands of people across the U.S. undergo dialysis—a life-sustaining but physically taxing treatment for kidney failure. These patients rely on dialysis centers to manage their care and keep them alive. But how do we know which facilities are doing well?

One key metric is **mortality rate**—the percentage of patients who die while under a facility’s care. Another is **transfusion rate**, which may indicate how often patients experience complications or severe anemia. This project explores whether transfusion rates (and other clinical indicators) can help predict mortality rates at dialysis centers.

---

## Why This Matters

Understanding the relationship between transfusions and mortality could help:

- Identify facilities that may need support or intervention
- Reveal early warning signs of poor outcomes
- Improve transparency and accountability in dialysis care

---

## The Data

We used publicly available data from the [Centers for Medicare & Medicaid Services (CMS)](https://data.cms.gov/provider-data/dataset/23ew-n7w9), which includes:

- **Mortality Rate**
- **Transfusion Rate**
- **Readmission Rate**
- **Hospitalization Rate**

Each row represents a dialysis facility in the U.S.

---

## The Questions We Asked

### 1. Does the transfusion rate at a facility relate to the mortality rate?

We started with a simple question: if a facility performs more transfusions, does that mean more of its patients are dying?

### 2. Can we predict mortality rate using other clinical indicators?

We wanted to see if a combination of metrics—transfusions, readmissions, and hospitalizations—could help us predict mortality more accurately.

### 3. Is transfusion rate alone enough to predict mortality?

We compared a full model (with all metrics) to a simple model using only transfusion rate.

---

## The Process (Non-Technical Summary)

1. **Data Cleaning**: We removed facilities with missing values in key metrics. This ensured our analysis was based on complete and reliable data.

2. **Exploration**: We visualized the distribution of each metric and looked for patterns. Histograms showed that most facilities had low mortality and transfusion rates, but a few had much higher values.

3. **Modeling**: We used a technique called **linear regression** to model the relationship between transfusion rate and mortality. We trained two models:
   - A **full model** using all three predictors
   - A **simple model** using only transfusion rate

4. **Evaluation**: We tested how well each model predicted mortality on unseen data and calculated the error rates.

---

## What We Found

- The full model predicted mortality with reasonable accuracy for most facilities.
- The simple model (transfusion only) was less accurate and missed important patterns.
- Some facilities had very high prediction errors, suggesting that other unmeasured factors (like patient demographics or staffing) may play a role.

---

## Key Takeaways

1. **Transfusions matter, but context is key**  
   Transfusion rate is a useful signal, but it works best when combined with other metrics.

2. **Outliers reveal complexity**  
   Some facilities had unusual patterns that couldn’t be explained by the available data.

3. **Correlation is not causation**  
   Just because transfusions and mortality are related doesn’t mean one causes the other.

---

## Final Thoughts

This project shows how data science can help us understand and improve healthcare. By analyzing publicly available data, we can uncover patterns that might otherwise go unnoticed—and help ensure better outcomes for patients who depend on dialysis to survive.
