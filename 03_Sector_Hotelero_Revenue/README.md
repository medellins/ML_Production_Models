# Machine Learning Ecosystem Applied to Hotel Revenue Management 🏨📈

This repository houses an advanced suite of predictive frameworks and pricing optimization engines developed under **Revenue Management** methodologies using **XGBoost**, **LightGBM**, and high-level interactive analytics via **Plotly**. The system addresses the most challenging business problems in the hospitality industry: seasonal demand forecasting and automated dynamic pricing to maximize RevPAR (Revenue Per Available Room).

---

## 📁 Operations Directory Architecture (MLOps)

The environment implements binary serialization and statistical matrix isolation. The production ecosystem automatically synchronizes under the following directory tree:

```text
03_Sector_Hotelero_Revenue/
├── datos_revenue_hotelero.csv      # Hotel historical operations dataset
└── modelo_revenue_hotelero.pkl     # Serialized binary and metadata of the pricing regressor
```

---

## 🏗️ Methodological Breakdown of Hospitality Solutions

### 💶 1. Dynamic Pricing Engine
*   **Business Case:** Automating the calculation of the daily optimal Best Available Rate (BAR) per night, maximizing property yields without cannibalizing demand volume across distribution channels (OTAs vs. Direct Booking).
*   **Methodology:** Advanced predictive engine powered by an **XGBoost Regressor**. The model processes highly dynamic real-time market features, such as the hotel's current occupancy percentage, reservation booking velocity (*Pick-up rate*), competitive price indexing (*CompSet*), and calendar seasonal constraints (month and day of the week).

### 📉 2. Inventory Imbalance Mitigation (No-Show & Attrition Management)
*   **Business Case:** Analytical modeling of early cancellations to optimize overbooking policies and protect the property's perishable inventory during high-demand peak seasons.

---

## 📊 Revenue Control Panels and Interactive Analytics (Plotly)

Statistical dashboards are built using **Plotly (Dynamic HTML)** enforcing a strict **four-decimal-place (`.4f`)** rounding format for both user interfaces and hover tooltips:

1.  **Actual vs. Recommended Pricing Timeline:** Short-term trend charts that visualize how the pricing engine adjusts recommendation algorithms up or down based on the daily booking pickup.
2.  **Demand Elasticity & Feature Weights:** Horizontal bar plots featuring exact relative weights (`.4f%`) fixed at the end of each bar to provide transparent business logic to General Managers.
3.  **Rate Deviation Histogram:** Error distribution chart styled with a soft blue palette (`#a6c8e0`) mathematically aligned with a theoretical **Gaussian Bell Curve** to audit for unbiased model residuals. Includes red operational threshold bands (e.g., ±5 €).
4.  **Seasonal Boxplot Deviations:** Interactive boxplots distributed by month of the year to track which specific travel seasons induce higher market volatility and prediction variance.

---
**Technical documentation developed under Machine Learning Engineering standards applied to hospitality revenue science.** 🚀
