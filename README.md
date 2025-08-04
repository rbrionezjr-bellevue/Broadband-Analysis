# Broadband Underserved Area Prediction

This project uses publicly available broadband deployment and income data to identify U.S. counties that are likely to remain underserved — defined here as lacking access to gigabit-speed internet (1000 Mbps download) — in the near future.

---

## 📘 Project Overview

Millions of households across the U.S. still lack access to high-speed broadband. Using FCC Broadband Data and U.S. Census income statistics, this project develops a machine learning model to predict which counties are likely to remain underserved in the next 6–12 months. These insights can help inform strategic fiber expansion efforts by identifying high-opportunity regions.

---

## 🔍 Data Sources

- **FCC Broadband Data Collection (2025)**  
  [Broadband Availability Data](https://www.fcc.gov/BroadbandData)

- **U.S. Census ACS S1903 (2024)**  
  [Median Household Income](https://data.census.gov/)

---

## 🧠 Modeling Approach

- **Features Used**:
  - Median household income (ACS)
  - Broadband availability at multiple speed tiers (FCC)
  - Total serviceable broadband units

- **Target**:
  - `has_gigabit`: Whether the county currently offers gigabit-level service (1000/100 Mbps)

- **Model**:  
  A **Random Forest Classifier** was trained on a merged and cleaned dataset of over 3,000 counties. The model was evaluated using stratified sampling to account for class imbalance.

---

## 📊 Key Visuals (from Notebook)

- Distribution of median household income (right-skewed)
- Coverage disparities in gigabit broadband availability
- Feature importance from Random Forest
- State-level map of predicted underserved counties

---

## ⚠️ Limitations

- FCC data is **self-reported** and may overstate coverage, particularly in rural areas.
- There is a **6–12 month lag** in deployment reporting.
- Dataset imbalance (many counties already report some gigabit service) makes accurate modeling difficult.
- Geographic alignment issues may arise due to data inconsistencies.

---

## 💡 Recommendations

- Use this model alongside other planning tools (e.g., permitting data, infrastructure maps).
- Prioritize improved data collection, especially verified provider availability.
- Incorporate block-level data in future work to increase precision.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `Broadband Analysis.ipynb` | Main Jupyter Notebook with data cleaning, EDA, modeling, and visualizations |
| `Broadband Analysis.pdf`   | Exported report with narrative summary, charts, and appendix |

---

## 🤝 Author

**Ruben Brionez Jr**  
_M.S. in Data Science candidate at Bellevue University_  
[LinkedIn Profile](https://www.linkedin.com/in/ruben-brionez-jr/)  
[GitHub Profile](https://github.com/rbrionezjr-bellevue)

---

## 📜 License

This project is provided for academic and educational use only.
