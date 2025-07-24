 1. Overview

This project analyzes the **“Cost of Living”** dataset, which provides detailed insights into average monthly income and living expenses across countries and years. By including both earnings and costs, the dataset enables a more comprehensive understanding of financial conditions worldwide.

- **Dataset Size:** 202 rows × 5 columns  
- **Final Size (after cleaning):** 199 rows × 5 columns

### Columns:
- `Country`: Name of each country (e.g., Australia, India, Russia)
- `Year`: Year of observation (ranging from 2000 to 2023)
- `Average_Monthly_Income`: Monthly income per person in USD
- `Cost_of_Living`: Estimated average monthly living expenses in USD
- `Region`: Geographical region (e.g., Asia, Europe, Africa, Oceania, etc.)

<img width="664" height="488" alt="Screenshot 2025-07-24 080849" src="https://github.com/user-attachments/assets/cb46a856-dafd-4b33-83d5-ccfdd91b7274" />

### Data Sources:
Although the original source is unspecified, the dataset likely compiles data from reputable institutions such as:
- **World Bank**
- **International Monetary Fund (IMF)**
- **International Labour Organization (ILO)**
- **Numbeo** (crowd-sourced and official statistics)

## 2. Data Cleaning

### Duplicate Records
- **Duplicates Found:** 2
- **Action Taken:** Removed both records.
- **Reasoning:** Duplicates can distort descriptive statistics and visuals. Ensuring each `Country-Year` pair appears only once improves accuracy and interpretability.

<img width="805" height="166" alt="Screenshot 2025-07-23 225341" src="https://github.com/user-attachments/assets/dd3db21b-e0d3-4e88-9d7a-71bf4392a484" />

### Missing Values

#### `Average_Monthly_Income`:
<img width="666" height="88" alt="Screenshot 2025-07-24 081855" src="https://github.com/user-attachments/assets/34a63e93-924b-49e8-bf7a-1446aa285424" />

- **Affected Rows:** 160, 176
- **Imputation Method:** Replaced with the **median** income value.
- **Why Median?** The median is more robust than the mean in datasets with extreme income disparities.
<img width="666" height="104" alt="Screenshot 2025-07-24 082232" src="https://github.com/user-attachments/assets/fd393373-082a-4aa5-b3b2-e7bb630fb7a8" />

#### `Region`:
<img width="666" height="76" alt="Screenshot 2025-07-24 082424" src="https://github.com/user-attachments/assets/d4a676cf-fb0e-4761-8797-3261e9cfde09" />
- **Affected Rows:** 26, 38
- **Fix:** Manual assignment based on known geography (e.g., Mexico → North America).
- **Purpose:** Maintains consistency in regional classification and avoids fragmentation in grouped analysis.
<img width="757" height="137" alt="Screenshot 2025-07-23 225445" src="https://github.com/user-attachments/assets/b87d9c67-6393-479b-84bb-be1a44ac364f" />

## 3. Descriptive Statistics
<img width="1015" height="386" alt="Screenshot 2025-07-24 082637" src="https://github.com/user-attachments/assets/d355dc48-cc02-4d59-ab47-938c5a7710be" />

- The high standard deviations indicate **significant economic disparities** across countries.
- Some countries enjoy a healthy income–cost gap, while others may face tight financial constraints.


## 4. Key Insights

### Insight 1: Income vs. Cost of Living

- A **scatter plot** reveals no strong linear relationship between income and living cost.
- Countries with high living costs don’t always have high incomes, and vice versa.
- Suggests that **income and cost of living vary independently** across nations.
<img width="960" height="490" alt="Screenshot 2025-07-24 180944" src="https://github.com/user-attachments/assets/a5e25e6b-3d35-44c2-82f4-77dbf55f8a25" />

### Insight 2: Regional Comparison

- A **bar chart** comparing total income and expenses by region shows:
  - **Europe** and **Asia** have the highest combined totals.
  - **North America** exhibits a **narrower income–expense gap**, suggesting tighter budgets.
- This reflects differences in **financial comfort** and **savings potential** across regions.
<img width="930" height="362" alt="Screenshot 2025-07-24 180934" src="https://github.com/user-attachments/assets/82ab515c-7f56-4f81-8f3f-52bca572a77a" />

---
