#  Predicting Global Electric Vehicle Adoption Trends Using Regression Models (2010–2023)

##  Overview
This project explores the global adoption of **electric vehicles (EVs)** using **supervised regression models**. It aims to analyze historical patterns in EV adoption and predict future sales shares based on past trends and hybrid vehicle adoption rates.  

The project leverages data from [Our World in Data](https://ourworldindata.org/electric-car-sales) covering the years **2010–2023**, focusing on how countries have embraced electric mobility over time.

---
View The Entire Notebook Analysis Here: https://nbviewer.org/github/BrentOchieng/global-ev-adoption-regression-analysis/blob/main/Predicting_Global_Electric_Vehicle_Adoption_Trends_Using_Regression_Models_%282010%E2%80%932023%29.ipynb

---

##  Project Objectives
1. **Predict the percentage share of electric cars sold in a given year** based on the previous year’s sales performance.  
2. **Predict the next year’s growth rate in electric car adoption** based on the current year’s electric car sales share.

---

##  Project Workflow
### 1. **Data Collection and Preparation**
- Dataset obtained from *Our World in Data (OWID)*.
- Cleaned and formatted data containing columns such as:
  - `Country`
  - `Year`
  - `Hybrid_Share`
  - `Electric_Share`
- Missing values were handled, and the dataset was filtered to ensure consistency across years.

### 2. **Exploratory Data Analysis (EDA)**
- Identified countries leading in EV adoption.
- Visualized trends in EV and hybrid sales over time.
- Created insights such as:
  - **Top 10 countries** with the highest EV sales share.
  - **Growth trajectories** of EV adoption from 2010–2023.
  - **Relationships** between hybrid and electric vehicle adoption.

### 3. **Feature Engineering**
- Created **lag features** (e.g., `electric_prev`) representing previous-year EV shares.
- Generated **growth rate variables** to capture year-over-year changes.
- One-hot encoded the `Country` column to handle categorical data.

### 4. **Model Building**
Implemented and compared three regression models:
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**

Each model was trained and tested using a stratified train-test split (80/20), with evaluation based on:
- Coefficient of determination (**R²**)
- Mean Squared Error (**MSE**)
- Visual comparison of actual vs. predicted values

---

##  Key Findings

### **Question 1: Predicting yearly EV sales share**
- **R² ≈ 0.90**, **MSE ≈ 6**
- Strong linear relationship between previous-year EV share and the current year’s share.
- Regression models achieved **excellent accuracy**, indicating that EV adoption follows consistent historical growth patterns.

### **Question 2: Predicting next-year EV growth rate**
- **R² ≈ 0.24**, **MSE ≈ 7.8**
- Moderate predictive performance — suggests short-term growth is influenced by external factors such as policy changes, fuel prices, and economic conditions.

---

## Interpretation
- The **high R² (0.9)** for the first objective shows that EV adoption is **predictable based on historical data**, following a strong upward trend.
- The **moderate R² (0.24)** for growth predictions highlights the need for additional external variables to improve predictive accuracy.
- **Ridge and Lasso regressions** performed similarly to Linear Regression, confirming model stability and low overfitting risk.

---

##  Tools & Technologies
| Category | Tools/Packages |
|-----------|----------------|
| **Language** | Python |
| **Libraries** | pandas, numpy, matplotlib, seaborn, scikit-learn |
| **Models Used** | Linear Regression, Ridge Regression, Lasso Regression |
| **Visualization** | Seaborn, Matplotlib |
| **Environment** | Jupyter Notebook |

---

##  Results Visualization
The project includes:
- **Bar plots** of top EV-adopting countries.
- **Line plots** showing adoption trends across years.
- **Scatter plots** comparing actual vs predicted electric vehicle shares.

---

##  Conclusion
This project demonstrates that:
- **Regression models** can effectively predict short-term EV adoption trends.
- Historical sales patterns are strong indicators of future market behavior.
- To enhance prediction accuracy, future work should incorporate:
  - **Socioeconomic indicators** (GDP, population, income levels)
  - **Policy data** (EV subsidies, carbon taxes, charging infrastructure)
  - **Advanced forecasting models** (Prophet, ARIMA, or hybrid ML approaches)



---

##  Citation
Dataset source:  
> Our World in Data (OWID), *Electric Car Sales and Market Share*.  
> Available at: [https://ourworldindata.org/electric-car-sales](https://ourworldindata.org/electric-car-sales)

---

##  Acknowledgements
Special thanks to **Our World in Data** for providing open access to high-quality sustainability datasets that make global analytics projects like this possible.

---


