# Deep Learning Ecosystem Applied to the Power & Energy Sector ⚡🧠

This repository contains an advanced production and validation framework for deep learning forecasting models implemented in **PyTorch** and **TensorFlow/Keras**. The ecosystem is engineered to address the most critical operational and financial challenges faced by modern utilities and transmission system operators (TSOs) within the energy transition framework.

---

## 📁 Production Directory Architecture

The framework is decoupled following software engineering and *MLOps* best practices. All historical structured datasets, network architectures, and inference binaries are automatically synchronized:

```text
01_Sector_Electricidad_Energia/
├── datos_series_temporales_deep_learning.csv   # Annual dataset for Project 1 (Solar)
├── datos_demanda_deep_learning.csv             # Annual dataset for Project 2 (Demand)
├── datos_precios_mercado_deep_learning.csv     # Monthly dataset for Project 3 (Pool Prices)
├── modelo_pytorch_solar_lstm.pkl               # LSTM Network Weights (PyTorch) - Proj 1
├── predicciones_pytorch_solar.pkl              # Validation metrics & arrays for Proj 1
├── modelo_tensorflow_demanda_cnn.h5            # 1D CNN Architecture & Weights (TF) - Proj 2
├── predicciones_tensorflow_demanda.pkl         # Validation metrics & arrays for Proj 2
├── modelo_pytorch_precios_mlp.pkl              # Deep MLP Weights (PyTorch) - Proj 3
└── predicciones_pytorch_precios.pkl            # Validation metrics & arrays for Proj 3
```

---

## 🏗️ Technical Breakdown of Industrial Solutions

### ☀️ 1. Renewable Generation Forecasting (LSTM Networks in PyTorch)
*   **Business Case:** Predicting hourly photovoltaic power curves (MW) to mitigate financial penalties from energy imbalance markets and optimize day-ahead pool bidding strategies.
*   **Architecture:** Recurrent Neural Network built with stacked two-layer **Long Short-Term Memory (LSTM)** cells, engineered to capture thermal inertia, cloud front advection, and irradiance ramp constraints.
*   **Data Engineering:** Time-series sequence formatting using a 24-hour continuous rolling window lookback, preprocessed with Min-Max scaling to prevent gradient saturation.

### 📉 2. Power Demand Forecasting (1D Convolutional Networks in TensorFlow)
*   **Business Case:** Load auditing to enable dispatch desks to efficiently schedule conventional thermal baseload and peaking units, preventing substation overloads and structural grid blackouts.
*   **Architecture:** Unidimensional Convolutional Neural Network (**1D CNN**) coupled with spatial reduction layers (`MaxPooling1D`) and deep dense layers in TensorFlow/Keras, designed to extract local seasonal human consumption micro-patterns.

### 💶 3. Wholesale Day-Ahead Market Modeling (Deep MLP in PyTorch)
*   **Business Case:** Forecasting pool price volatility (€/MWh) and anticipating scarcity events (*Price Spikes*) to hedge financial risk for energy trading desks.
*   **Architecture:** Deep **Multilayer Perceptron (MLP)** in PyTorch with sequential dense layers and active **Dropout (15%)** regularization to filter out auction market noise and structural anomalies.
*   **Financial Feature Injection:** Coupling international commodity cost curves (Natural Gas and $CO_2$ Emission Allowances) with market structural lags (`Precio_Lag1`, `Precio_Lag24`).

---

## 📊 Analytical Control Dashboards (Plotly MLOps)

The project features a production-grade visual layout, replacing conventional static plots with dynamic, interactive **Plotly (HTML)** dashboards:

1.  **Time Series Control Panel:** Direct comparison of actual vs. predicted curves using a unified X-axis hover system (`hovermode='x unified'`) and fixed trace naming for clear dispatch audits.
2.  **Gaussian Residual Analysis:** Error histogram customized with a corporate soft blue palette (`#a6c8e0`), mathematically superposed with a theoretical continuous **Gaussian Bell Curve** calculated via probability density. Includes industrial tolerance lines to identify financial bias.
3.  **Temporal Boxplot Audit:** Interactive boxplots segmented by day of the week to evaluate AI drift dispersion between industrial business days and weekend demand pullbacks.

---

## 🧮 Evaluation Metrics and Strict Precision (.4f)

Both Plotly chart hover tooltips and the corporate audit logs enforce a strict **four-decimal-place (`.4f`)** rounding format for global business KPIs: **MAE**, **MSE**, **RMSE**, and **R² Score**, ensuring precision-grade mathematical traceability.

---
**Engineered under strict Machine Learning Engineering guidelines for the utilities sector.** 🚀
