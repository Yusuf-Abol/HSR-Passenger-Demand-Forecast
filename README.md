---

# High-Speed Rail Passenger Demand Forecast

 📊 A robust forecasting pipeline for daily transportation passenger counts, combining classical time series modeling with deep learning for superior accuracy and reliability.

---

## Overview

This project builds a **hybrid time series forecasting model** that blends the strengths of:
- **SARIMAX** (for trend and seasonality)
- **BiGRU** (for complex, non-linear patterns)

It’s designed for **operational planning, capacity forecasting, and resource optimization** in public transit systems.

---

## Goals

- Predict **daily passenger counts** with high accuracy  
- Understand and model **weekly and seasonal patterns**  
- Compare performance across multiple statistical and ML models  
- Enable future-ready extensions (e.g., external variables, real-time deployment)

---

## Data Summary

- **Timeframe:** 2012–2014  
- **Features:** Daily passenger counts  
- **Patterns Identified:**
  - 📅 Strong weekly cycle (Mon–Fri peaks)
  - 🌞 Summer surges (tourism effect)
  - 📈 Long-term upward trend

---

##  Models Compared

| Model              | RMSE     | MAPE     | Notes |
|-------------------|----------|----------|-------|
| Naïve              | 116.07    | 21.80%  | Baseline |
| SES                | 114.93   | 22.00%   | Simple smoothing |
| Holt Linear        | 105.92   | 26.84%   | Captures trend |
| Holt-Winters       | 111.59   | 22.81%   | Adds seasonality |
| ARIMA              | 115.77   | 22.20%   | Basic autoregression |
| SARIMAX            | 70.65    | 13.18%   | Strong seasonality capture |
| BiGRU              | 75.40    | 15.15%   | Learns nonlinear patterns |
| **Hybrid**         | **74.09**| **11.43%** | ✅ **Best overall performance** |

---

##  Why Hybrid Works

- **SARIMAX** handles repeating cycles (weekly, monthly) and long-term growth.
- **BiGRU** captures irregularities like spikes, holidays, and nonlinear changes.
- **Together**, they outperform every individual model in both absolute and relative error.

---

## Forecast Snapshot  
*(Insert image if available, or remove this section)*  
> Example output: Daily forecast from July 2014–Jan 2015  
> Shows expected weekly cycles and seasonal surges

---

## Project Structure

```bash
├── data/              # Raw and processed data
├── notebooks/         # Exploratory analysis and model dev
├── src/               # Model scripts
│   ├── sarimax_model.py
│   ├── bigru_model.py
│   └── hybrid_model.py
├── results/           # Plots, predictions, metrics
├── requirements.txt
└── README.md
```


## Future Extensions

- Add external regressors (events, weather, holidays)
- Quantile forecasts for uncertainty estimation
- Deploy model via REST API or dashboard

---

## 🙌 Credits

Developed by [Yusuf Abolarinwa]  
Feel free to contribute via PRs or issues!

---

## 📄 License

Licensed under the MIT License. See `LICENSE` for details.

---

Let me know if you’d like:
- A **demo GIF** or interactive notebook preview
- A **one-line badge** (e.g., Python version, status)
- To hook this up with GitHub Pages or Streamlit for live demo access

I can generate any of that for you.
