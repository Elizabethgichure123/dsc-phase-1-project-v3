# 🛩️ Aviation Safety Risk Analysis

##  Project Overview
This project investigates aviation accident data to help a company decide which aircraft types pose the lowest operational risks. The goal is to inform safe and strategic decisions as the company considers entering the aviation industry.

---

##  Business Understanding

Aviation Company Limited plans to diversify by investing in the aviation sector. However, limited knowledge about aircraft safety poses a challenge. This project aims to identify which aircraft makes and models present the **lowest risk profiles**, using historical accident data.

---

##  Data Source

- **Dataset**: National Transportation Safety Board (NTSB) Aviation Accident Database (1962–2023)
- **Key Fields Used**:
  - `Make`, `Model`, `Aircraft.damage`, `Injury.Severity`
  - `Total.Fatal.Injuries`, `Total.Serious.Injuries`, `Total.Minor.Injuries`, `Total.Uninjured`
  - `Country`, `Event.Date`, `Aircraft.Category`

---

##  Data Preparation

- Combined aircraft make and model into a unified field
- Replaced missing categorical values with the **mode**
- Replaced missing numerical values with the **mean**
- Extracted `Event_Year` from `Event.Date`
- Computed a custom `Risk_Score` using weighted injury severity:
  
  \[
  \text{Risk Score} = (\text{Fatal Injuries}) + 0.5 \times (\text{Serious Injuries}) + 0.2 \times (\text{Minor Injuries})
  \]

---
## Data Visualization: Tableau Interactive Dashboard

https://public.tableau.com/app/profile/elizabeth.gichure6005/viz/Phase_1Project/Dashboard1?publish=yes


##  Key Insights

### 1. Top 10 Aircraft with High Frequency and Low Risk
Aircraft models that appear often in the dataset but have low risk scores — ideal candidates for investment.

---

### 2. Aircraft Status Post-Accident
Most aircraft are categorized as either "Substantial" or "Destroyed" after incidents.

---

### 3. Accident Trends Over Time
Visualizing total accidents from 1962 to 2023 shows a decline in recent years.

---

### 4. Countries with Lowest Accident Counts
Some African countries report significantly fewer incidents, suggesting lower exposure or underreporting.

---

##  Business Recommendations

1. **Invest in common aircraft types with low risk scores**, such as [Insert actual aircraft names from your top 10 list].
2. **Prioritize models associated with non-fatal incidents** to improve safety profiles.
3. **Start operations in countries with historically lower incident rates** — these regions may offer safer or less competitive environments.

---

##  Tools Used

- Python (Pandas, Matplotlib)
- Jupyter Notebook
- Tableau Public
- GitHub

---

Liz — Data Science Student, Flatiron School (Phase 1 Project)
