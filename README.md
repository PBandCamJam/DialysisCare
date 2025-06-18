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
| Field | Description|
|**Source** | (https://data.cms.gov/provider-data/dataset/23ew-n7w9) |
| Scope | Hundreds of U.S. dialysis facilities |
| Key Variables Used | *Mortality Rate*, *Readmission Rate*, *Hospitalization Rate*, *Trasnfusion Rate* |
