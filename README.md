# Toyota Corolla Price Prediction: Multiple Linear Regression Analysis 🚗

## 📌 Project Overview
This project applies Multiple Linear Regression to predict the resale value of used Toyota Corollas. By identifying the core mechanical and usage-based drivers of depreciation, this model provides automotive dealerships with a data-driven framework to automate trade-in valuations, optimize pricing strategies, and protect profit margins.

## 📊 Dataset Description
The dataset comprises various physical and mechanical attributes of Toyota Corollas to evaluate their impact on market price.
* **Target Variable (Dependent):** `Price` (in Euros)
* **Key Predictor Variables (Independent):** * `Age_08_04`: Age of the vehicle in months.
  * `KM`: Accumulated kilometers (odometer reading).
  * `Weight`: Vehicle weight in kilograms.
  * `HP`: Engine horsepower.
  * *Note: Initial exploratory variables also included `Doors` and `Gears`.*

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (Multiple Linear Regression, metrics)
* **Data Visualization:** `matplotlib`, `seaborn`

## 🧠 Methodology & Iterative Modeling
A key focus of this project was feature selection to prevent overfitting and ensure model simplicity.

1. **Exploratory Data Analysis (EDA):** Generated correlation heatmaps and pairplots to identify multicollinearity and linear relationships between predictors and the target price.
2. **Model 1 (Baseline):** Trained an initial Multiple Linear Regression model using all available features. Hypothesis testing (evaluating p-values) revealed that `Doors` and `Gears` were not statistically significant predictors of the vehicle's price.
3. **Model 2 (Refined):** Dropped the insignificant features (`Doors`, `Gears`) to build a refined model. This iterative step simplified the mathematical equation while maintaining a highly comparable predictive power, resulting in a more robust model for real-world deployment.
4. **Model Diagnostics:** Validated the refined model using residual plots to confirm homoscedasticity and ensure errors were randomly distributed.

## 📈 Key Results & Performance (Model 2)
The refined model successfully isolates the true drivers of vehicle depreciation.

* **R-Squared (R²):** 0.859
* **Root Mean Squared Error (RMSE):** 1239.03
* **Feature Coefficients (Impact on Price):**
  * **Age:** Decreases value by `120.44` per month.
  * **KM:** Decreases value by `-0.019` per kilometer.
  * **Weight:** Increases value by `€ 19.7` per kilogram.
  * **HP:** Increases value by `€ 38.59` per unit of horsepower.

## 💼 Business Impact
* **Appraisal Automation:** Enables instant, data-backed trade-in appraisals, reducing human error and appraisal time.
* **Inventory Strategy:** Allows dealerships to accurately forecast the holding depreciation of their current stock.
* **Pricing Optimization:** Ensures vehicles are priced competitively according to live market features rather than static estimations.

