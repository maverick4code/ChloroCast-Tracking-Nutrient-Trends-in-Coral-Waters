# 🌿 Predicting Chlorophyll Concentrations Using Regression Models

## 🌊 Project Overview(This is just my Leraning Project)

This project explores how we can use regression models to predict chlorophyll concentrations in coastal waters, specifically at the Burdekin River site. Since chlorophyll levels are a key indicator of water quality, tracking and forecasting them can help us detect nutrient pollution and protect nearby ecosystems like coral reefs.

By modeling chlorophyll concentration over time and across seasons, we aim to gain insights that can support environmental monitoring and marine conservation efforts.

---

## 📚 Table of Contents

* [Objective](#🌟-objective)
* [Data](#🧪-data)
* [Methodology](#🔍-methodology)
* [Modeling](#🧠-modeling)
* [Results](#📉-results)
* [Conclusion](#✅-conclusion)
* [Installation](#⚙%ef%b8%8f-installation)
* [Usage](#🚀-usage)

---

## 🌟 Objective

Here’s what I set out to do:
* Build a regression model to predict chlorophyll concentration based on time.
* Understand how seasonal patterns influence chlorophyll levels.
* Evaluate the models using metrics like Mean Absolute Error (MAE) to see how accurate our predictions are.

---

## 🧪 Data

I used a dataset that includes chlorophyll concentration measurements (`CHL_QA_AVG`) collected from the Burdekin River site. Each data point comes with:
* Chlorophyll concentration in micrograms per liter (µg/L)
* Sampling date (`SAMPLE_DAY`)
* Station ID (`STATION_ID`)

To make the modeling easier, I also processed the data to include:
* A day-wise index (`idx`) to represent time sequentially
* A `MONTH` column to capture seasonal variations

---

## 🔍 Methodology

I have explored two regression models:
* **Simple Linear Regression** – Just the day index (`idx`) is used to predict chlorophyll levels.
* **Multiple Linear Regression** – I included both the day index and the month to account for seasonal trends.

All models were built using the `statsmodels` library in Python.

---

## 🧠 Modeling

### 📈 Simple Linear Regression

*Creating a simple linear regression model to predict chlorophyll concentration using the day number (`idx`) as the predictor.*

This helped us get a baseline understanding of the long-term trend.

### 📊 Multiple Linear Regression

*Creating a multiple linear regression model using both the day number (`idx`) and the month (`MONTH`) as predictors.*

By adding the seasonal component, here I aimed to improve the model's ability to capture real-world fluctuations in chlorophyll levels.

---

## 📉 Model Evaluation

To evaluate the models, we looked at:
* **R-squared values** to check how well the models explain the variance in the data
* **Residuals** to identify any systematic errors
* **Mean Absolute Error (MAE)** to measure prediction accuracy

> The lower the MAE, the better the model performs.

---

## 📊 Results

Here’s what I have found:
* The simple model captured the overall trend decently.
* The multiple regression model performed better by factoring in seasonal shifts.

**Model MAE comparison:**
* Simple Linear Regression: \~0.257
* Multiple Linear Regression: \~0.2497

Even a small improvement like this can be meaningful when monitoring environmental indicators over time.

---

## ✅ Conclusion
This project highlights how even basic regression models can provide valuable insights into environmental trends. Including seasonal variables made a noticeable difference in prediction accuracy.

**Next Steps:**
In the future, I’d love to explore more complex models or bring in additional data like temperature, rainfall, or sediment levels. This could further boost accuracy and help in proactive environmental management—especially in regions close to sensitive ecosystems like coral reefs.

---

## ⚙️ Installation

To get started:

**Clone this repo:**

```bash
git clone https://github.com/maverick4code/ChloroCast-Tracking-Nutrient-Trends-in-Coral-Waters
```

**Install the required Python libraries:**

```bash
pip install -r requirements.txt
```

---


If you have suggestions or ideas to build on this project, contributions are more than welcome! Let’s use data to better understand and protect our environment 🌍
