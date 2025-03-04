**Customer Lifetime Value (CLV) Prediction for Hotels** 

**Project Overview**

This project predicts Customer Lifetime Value (CLV) in the hotel industry using Machine Learning (XGBoost & Random Forest). CLV represents the total revenue a hotel can expect from a customer over their relationship period. This analysis helps hotels identify high-value customers, optimize marketing strategies, and enhance revenue management.

**Why CLV Prediction?**

Identifies repeat high-value customers for loyalty programs & personalized offers.

Helps hotels adjust pricing & promotions to maximize profitability.

Enables targeted marketing by predicting which customers are likely to generate more revenue.

**Key Steps in This Project**

**1️⃣ Data Preprocessing & Feature Engineering**

1. Loaded and cleaned the Hotel Booking Business Analytics dataset.
  
2. Created total_nights feature (weekend + weekday stays).
  
3. Defined CLV formula: CLV = ADR × Total Nights × (Previous Bookings Not Canceled + 1)
 
4. Selected features impacting CLV:

ADR (Average Daily Rate)

Total Nights Stayed

Lead Time (Booking Behavior)

Previous Bookings Not Canceled 

**2️⃣ Model Training & Evaluation**

Random Forest Regressor as a baseline model

XGBoost Regressor for improved performance

Feature Importance Analysis to determine key CLV drivers

**3️⃣ Model Performance Comparison**

| Model          | MAE ↓ (Lower Better) | MSE ↓ (Lower Better) | RMSE ↓ (Lower Better) | R² ↑ (Higher Better) |
|---------------|----------------------|----------------------|----------------------|----------------------|
| **Random Forest** | **3.78** | 6728.86 | 82.03 | 0.9721 |
| **XGBoost**      | 9.94  | **4809.16** | **69.35** | **0.9801** |


**Insights from Model Comparison:**

✔ XGBoost performed best, achieving highest accuracy (R² = 0.9801) and lowest RMSE (69.35).

✔ Random Forest had lower MAE (3.78), meaning it minimized smaller errors better.

✔ Overall, XGBoost is the most effective model for hotel CLV prediction.

**4️⃣ Feature Importance (XGBoost Analysis)**

The most influential factors driving CLV are:

✔ Previous Bookings Not Canceled (~40%) → Repeat customers are most valuable.

✔ Total Nights Stayed (~30%) → Longer stays significantly impact revenue.

✔ ADR (Average Daily Rate) (~20%) → Higher ADR correlates with higher CLV.

✔ Lead Time (~5%) → Advance bookings slightly affect CLV.

✔ Cancellation Status (~0%) → Negligible impact, suggesting frequent bookers compensate for occasional cancellations.

**5️⃣ Business Impact:**

Target repeat guests with loyalty programs.

Optimize pricing models for long-stay customers.

Adjust marketing efforts toward high-value customers.

## Tech Stack

| Category                  | Technology Used  |
|--------------------------|----------------|
| **Programming Language** | Python |
| **Data Processing** | Pandas, NumPy |
| **Machine Learning Models** | XGBoost, Random Forest |
| **Model Evaluation** | Scikit-Learn (MAE, RMSE, R²) |


**Conclusion**
This project demonstrates data-driven CLV prediction using Machine Learning, helping hotels identify and retain high-value customers. By leveraging XGBoost & Random Forest, we accurately forecast guest revenue potential, enabling optimized pricing, marketing strategies, and personalized customer experiences.

