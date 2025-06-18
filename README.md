# Death and Dialysis

A linear regression project exploring the relationship between **transfusion rates** and **mortality rates** in dialysis facilities across the U.S.

![image](https://github.com/user-attachments/assets/761508c9-e5a7-49b4-85b6-f536385d09ec)

Each day, there are thousands of people that sit for hours on end. They get their blood cleaned by machines in an exhausting routine that keeps them alive.
For dialysis providers, the most important metric is their patient's mortality rate. Keeping these rates low is the driving force of any facility.

It's a pretty simple concept, and it begs the question:
> **Does the frequency of blood transfusions at a faclility hint at how many of its patients ultimately survive?**

More transfusions often signal sicker patients or urgent complications.
By examining transfusion rates alongside readmission rates and hospitalization rates, I set out to see whether these metrics can predict mortality differences from one clinic to the next.

---

## Background and Motivation
Dialysis is lifesaving, yet high-risk. Centers for Medicare & Medicaid Services (CMS) publicly tracks how each facility performs on metrics such as readmissions, hospitalizations, transfusions, and mortality.
If certain operational patterns reliably foreshadow higher death rates, providers could intervene earlier and target support more precisely.

This project explores whether a linear regression model can turn these routinely reported metrics into early warning signals.

---

## Dataset
**Source**: (https://data.cms.gov/provider-data/dataset/23ew-n7w9)  
Scope: Hundreds of U.S. dialysis facilities  
Key Variables Used: *Mortality Rate*, *Readmission Rate*, *Hospitalization Rate*, *Trasnfusion Rate*

---

## Modeling Approach
- **Language/Tools**: Python 3, Jupyter, 'pandas', 'numpy', 'scikit-learn', 'matplotlib'
- **Train/Test Split**: 80/20 using random_state=12
- **Model**: Linear Regression

---

## Results
Relative Errors: 2.36448865%, 46.51394902%, 89.42139739%,  7.16557005% 28.83239043%,  3.52098489% 33.59703882%,  3.30336793%, 6.46676561%,  5.13622335%

### Quick Takeaways
- Most facilitiess were predicted within 10%, which is encouraging for a simple model.
- A handful were **extremely off** (between a ~30-90% error), showing that there are unmeasured factors.
- Hospitalization and readmission rates combined with transfusion rates give round out the affect on mortality rate.

---

## Key Insights
1. **Transfusions matter, but the context is key**: They're a meaningful insight into patient mortality, but adding hospitalization and readmssion rates improves reliability.
2. **Outliers reveal hidden complexity**: Facilities aren't black and white. There are a lot of contributing factors that could cause a simple model to not accurately reflect a facilities mortality rates.
3. **Correlation is not Causation**: Higher transfusion rates correlate with higher mortality, but transfusions themselves aren't the cause.

---
