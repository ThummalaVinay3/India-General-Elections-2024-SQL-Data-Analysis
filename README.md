# India-General-Elections-2024-SQL-Data-Analysis
This project provides an in-depth **SQL-based analysis** of the **2024 Indian General Elections** dataset.   It uses multiple datasets such as constituency-level results, party-wise statistics, and state-wise outcomes to uncover insights about seat distributions, alliances, vote margins, and election performance across India.


---

## 📊 Project Overview

The goal of this project is to analyze and visualize data from the 2024 Indian General Elections using **SQL Server**.  
Through SQL queries and data exploration, we identify the top-performing alliances, party distributions, and detailed constituency results.

---

## 📁 Datasets Used

| File Name | Description |
|------------|--------------|
| `constituencywise_details.csv` | Candidate-level details including votes (EVM & Postal) |
| `constituencywise_results.csv` | Constituency-level winning candidates and parties |
| `partywise_results.csv` | Party-wise total seats won and performance data |
| `statewise_results.csv` | State-level mapping of constituencies and results |
| `states.csv` | State reference data used for joins and grouping |

---

## ⚙️ Tools & Technologies

- **Microsoft SQL Server (SSMS)**
- **SQL (T-SQL Queries)**
- **Data Cleaning and Joins**
- **Dataset Integration using Foreign Keys**

---

## 🧠 Key SQL Queries & Insights

1. **Total Seats and State-wise Seats**  
   → Counted total constituencies and seats available per state.

2. **Alliance Analysis (NDA, I.N.D.I.A, Others)**  
   → Calculated total seats won by each major alliance.

3. **Party-level Performance**  
   → Identified top-performing parties across all states.

4. **Candidate Insights**  
   → Extracted winning and runner-up candidates in each constituency.

5. **Vote Distribution**  
   → Compared EVM votes vs Postal votes in selected constituencies.

6. **State-specific Analysis (e.g., Andhra Pradesh, Karnataka)**  
   → Derived total votes, number of candidates, and alliance performance per state.

---

## 🧩 Data Processing Highlights

- Added a new column **`party_alliance`** in `partywise_results` table to classify parties into:
  - `NDA`
  - `I.N.D.I.A`
  - `OTHER`

- Joined multiple datasets using:
  ```sql
  constituencywise_results
  JOIN partywise_results
  JOIN statewise_results
  JOIN states
