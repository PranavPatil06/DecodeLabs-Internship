# 🛒 E-Commerce Sales Prediction & Analytics Pipeline
**Decodelabs Data Science Internship Project**

## 📖 Project Overview
This repository contains an end-to-end Data Science and Machine Learning pipeline built for an e-commerce platform. The project spans the entire data lifecycle: from raw data ingestion and cleaning to exploratory data analysis (EDA), business intelligence dashboarding, and the deployment of a predictive machine learning model.

The primary objective of this project is to extract actionable business insights regarding marketing ROI and operational health, and to engineer an algorithm capable of predicting a customer's total cart value based purely on behavioral features.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Random Forest)
* **Environment:** Jupyter Notebook

## 📊 The Dataset
The dataset represents 1,200 unique customer transactions, containing 14 distinct features spanning logistics, marketing, and financial data. 
* **Key Features:** `Product`, `ItemsInCart`, `PaymentMethod`, `ReferralSource`, `CouponCode`, `OrderStatus`, `TotalPrice`
* **Data Quality:** Handled missing marketing data (unapplied coupons) to preserve transaction integrity and reformatted temporal data for time-series analysis.

## 🚀 Methodology & Project Workflow

### 1. Data Cleaning & Preprocessing
* Removed system duplicate entries to prevent skewed revenue metrics.
* Transformed string-based transaction dates into standardized datetime objects.
* Handled null values logically (e.g., replacing missing `CouponCode` fields with 'No Coupon' to indicate full-price purchases).

### 2. Exploratory Data Analysis (EDA)
* Conducted statistical summarization to understand baseline customer behavior.
* Deployed **Boxplots** to verify the absence of extreme pricing anomalies/outliers.
* Built **Bar Charts** to identify top-moving inventory (Printers, Tablets, Chairs).
* Mapped customer cart behavior using color-coded **Scatterplots** to understand the correlation between cart size and payment methodology.

### 3. Business Intelligence Dashboarding
Designed a presentation-ready visual dashboard focusing on three core business pillars:
* **Marketing ROI:** Aggregated total revenue by `ReferralSource` to pinpoint the most profitable marketing channels.
* **Operational Health:** Visualized supply chain success via a Donut Chart tracking `OrderStatus` (Shipped vs. Returned vs. Cancelled).
* **Company Growth:** Plotted a time-series line chart tracking monthly revenue trends to identify seasonal spikes.

### 4. Predictive Machine Learning Model
Engineered a **Random Forest Regressor** to predict the `TotalPrice` of a customer's order.
* **Feature Engineering:** Deliberately excluded explicit mathematical features (`Quantity` and `UnitPrice`) to force the algorithm to learn genuine behavioral patterns rather than memorizing basic arithmetic.
* **Encoding:** Transformed categorical string data (marketing channels, payment methods) using One-Hot Encoding (`pd.get_dummies`).
* **Model Performance:** Achieved a Mean Absolute Error (MAE) of **~$646**, establishing a strong baseline for behavioral price prediction in a highly variable dataset.

## 💻 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/PranavPatil06/DecodeLabs-Internship.git](https://github.com/PranavPatil06/DecodeLabs-Internship.git)
   cd DecodeLabs-Internship

2. **Create a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt

4. **Launch Jupyter:**
   ```bash
   jupyter notebook


## 👨‍💻 Author
**Pranav Patil** | Computer Engineering Student | Data Science Intern at Decodelabs
