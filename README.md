# Time-Series-Forecasting-for-Skyrose-Beverages-Canada-
The analysis and forecasting models developed for the Skyrose Marketing Agency to address key challenges faced by their beverage industry clients in Canada. The project provides forecast-driven insights for inventory, marketing, and strategic decision-making.

## 🎯 Project Goals and Business Context

The forecasting project was initiated to address key challenges faced by the Skyrose Marketing Agency and its clients:

* **Client Focus:** Skyrose works with Vintage Vino (White Wine), On The Rocks (Whisky), and is prospecting Downtown Brew Co. (Craft Beer).

* **Operational Challenges:** The agency experienced heavy workload cycles during peaks (e.g., holidays) and underutilization during quiet periods.

* **Data Limitation:** Previous Google Trends data exploration was relative and not tied directly to sales, limiting its utility for planning.

* **Primary Objectives:**
    
    * Analyze weekly sales data for the three main beverages.
    
    * Identify sales patterns, trends, and seasonality.
    
    * Evaluate and compare forecasting models to recommend the best approach for each product line.

## 📁 Data and Methodology

The analysis was based on weekly sales data collected over approximately **262 weeks** (August 2020 to August 2025) across **Canada**.

### Data Characteristics & Preparation

* **Products:** White Wine, Whisky, and Craft Beer.

* **Data Split:** The dataset was partitioned into 80% for training the models and 20% for testing their performance.

### Methodology Used

* **Stationarity Check:** The Augmented Dickey-Fuller (ADF) test was used to confirm that the time series data for all products was stationary.

* **Decomposition:** Time Series Decomposition was performed to isolate the Trend, Seasonality, and Residual components.

* **Models Evaluated:** A wide range of models were implemented for comparison, including:
    
    * Moving Average (MA) models (3-, 6-, 9-, 12-week windows).
    
    * Exponential Smoothing (ES) models (Simple ES, Holt's Trend, Holt-Winters).
    
    * ARMA Modeling (using `auto_arima` for parameter selection).

* **Evaluation Metrics:** Model accuracy was measured using **MSE** (Mean Squared Error), **MAE** (Mean Absolute Error), and **MAPE** (Mean Absolute Percentage Error).

## 📊 Product-Specific Forecasting Results

The optimal forecasting model and key insights varied significantly by beverage:

### 🍷 White Wine (Vintage Vino)

* **Seasonality:** Exhibits strong seasonal peaks around **Week 26** (late spring/early summer).

* **Best Model:** **Holt-Winters Seasonal Smoothing**.

* **Performance:** It was the best performer, achieving a MAPE of **4.93%** and an MSE of **3.25**.

* **Forecast:** The model projects steady growth with seasonal peaks continuing around Week 26.

### 🍺 Craft Beer (Downtown Brew Co.)

* **Trend:** The series shows an overall **declining trend** with annual seasonal peaks.

* **Best Model:** **3-Week Moving Average**.

* **Performance:** The 3-Week MA achieved the lowest MSE (**0.29**) and MAE (**0.43**).

* **Forecast:** The model suggests a continued downward trend with smaller seasonal spikes, effectively capturing recent short-term changes.

### 🥃 Whisky (On The Rocks)

* **Seasonality:** Characterized by sharp, strong peaks at **Week 51-52** (the holiday season).

* **Trend:** Shows consistent **upward growth** in sales over the long term.

* **Best Model:** **Holt-Winters Seasonal Smoothing**.

* **Performance:** This model was the best across all metrics for Whisky, achieving the lowest MAPE of **4.87%**.

* **Forecast:** Projects strong holiday season peaks and confirms an upward long-term trend, indicating growing popularity.

## 💡 Key Recommendations and Business Impact

The forecast-driven planning enables Skyrose to align production, inventory, and marketing efforts strategically.

### Strategic Recommendations

* **Inventory Optimization:**
    
    * **White Wine:** Build inventory before the late spring/early summer peak (Week 26).
   
    * **Whisky:** Increase capacity and distribution before the holiday season (Week 51-52).
    
    * **Craft Beer:** Gradually reduce production while staying flexible for short-term spikes.

* **Marketing Strategy:**
    
    * Launch targeted campaigns around forecasted peaks (e.g., whisky before holidays, wine in early summer).
    
    * Use bundling or cross-promotions during high-demand seasons.

* **Product Strategy:**
    
    * **Craft Beer:** Diversify or refresh the portfolio to actively counter the observed sales decline.
    
    * Reassess distribution channels to match the significant forecasted spikes, especially for high-growth products like Whisky.

### Business Impact

* **Inventory Optimization:** Leads to reduced stockouts during high demand and less overproduction during low periods.

* **Marketing Timing:** Ensures better alignment of campaigns with peak demand periods.

* **Revenue Growth:** Seasonal insights can be leveraged for more effective promotions and higher sales.
