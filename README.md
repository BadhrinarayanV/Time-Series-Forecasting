
# 📈 Electric Production Forecasting using Time Series Models

This project aims to forecast electric production using various time series models. We explored traditional statistical models like SARIMAX and Holt-Winters, and finally built an ensemble model using Linear Regression to improve forecast accuracy.

The goal is to understand seasonal patterns and trends in electricity production and identify the most accurate forecasting technique.

## 📊 Dataset

- Source: [Kaggle]
- Columns: `DATE`, `IPG2211A2N`
- Total Records: ~30 years of monthly electric production data.
- Frequency: Monthly

We converted the `DATE` column to datetime format and used it as the index for time series modeling.

## 🧠 Models Used

1. **SARIMAX (Seasonal ARIMA with exogenous variables)**
   - Captures trend and seasonality.
   - Evaluated using ADF test, ACF, and PACF plots.

2. **Holt-Winters Method**
   - Exponential smoothing for trend and seasonality.

3. **Ensemble Model**
   - Combined forecasts of SARIMAX and Holt-Winters using Linear Regression.
   - Aims to reduce error by stacking.

## 📏 Evaluation Metrics

We used the following metrics to evaluate the model performance:

- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**

| Model         | MAE   | RMSE  |
|---------------|-------|-------|
| SARIMAX       | 4.10  | 5.83  |
| Holt-Winters  | 3.27  | 4.23  |
| Stacked Model | 2.54  | 3.26  |

The stacked model provided the lowest error, making it the most effective approach in this project.

## ⚙️ Requirements

To run the notebook, install the following packages:

```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
```

## ✅ Conclusion

- Time series forecasting requires careful analysis of trends, seasonality, and stationarity.
- SARIMAX and Holt-Winters individually performed well, but the stacked model outperformed them in terms of MAE and RMSE.
- This project enhanced my understanding of ensemble techniques for time series data.

## 👨‍💻 Author

**Badhrinarayan V**  
Data Science Intern
D Square Analytix
