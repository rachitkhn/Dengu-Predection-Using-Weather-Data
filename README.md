# 🦟 Dengue Case Prediction Using Weather Data

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-green?style=flat-square&logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

> A machine learning project forecasting dengue fever case volumes from 26 environmental and weather attributes — enabling health authorities to proactively allocate resources and intervene before outbreaks escalate.

---

## 📌 Project Overview

Dengue fever is a mosquito-borne illness affecting millions globally, with transmission rates heavily influenced by environmental conditions. Temperature, humidity, rainfall, and solar radiation all affect mosquito breeding cycles and population dynamics — making weather data a powerful, readily available signal for disease forecasting.

This project builds a predictive ML model trained on historical weather records to forecast dengue case volumes and classify outbreak risk levels. By providing early warning signals from environmental data alone, the model supports public health officials in making timely, evidence-based decisions about resource deployment and preventative interventions.

---

## 🎯 Objectives

- Identify the environmental and meteorological features most strongly correlated with dengue transmission
- Build regression models to forecast case counts based on weather data
- Build classification models to label outbreak risk levels (low / medium / high)
- Deliver a data-driven early warning tool to support public health planning

---

## 📂 Repository Structure

```
Dengue-Prediction-Using-Weather-Data/
│
├── Dengue Case Prediction.ipynb    # Full ML pipeline: EDA → preprocessing → modelling → evaluation
├── dengue_data.csv                 # Historical weather and dengue case records dataset
├── README.md
└── LICENSE
```

---

## 📊 Dataset

The dataset contains historical records with **26 weather and environmental attributes** linked to confirmed dengue case counts:

### Temperature Metrics
| Feature | Description |
|---|---|
| `tempmax` | Maximum daily temperature (°C) |
| `tempmin` | Minimum daily temperature (°C) |
| `temp` | Average daily temperature (°C) |
| `feelslike` | Perceived temperature accounting for humidity and wind |

### Humidity & Moisture
| Feature | Description |
|---|---|
| `humidity` | Relative humidity (%) — critical for mosquito survival |
| `dew` | Dew point temperature — indicator of atmospheric moisture |

### Precipitation & Atmosphere
| Feature | Description |
|---|---|
| `precip` | Daily rainfall (mm) — affects standing water availability for breeding |
| `cloudcover` | Cloud coverage (%) — impacts solar radiation and temperature |
| `visibility` | Atmospheric visibility (km) |
| `sealevelpressure` | Barometric pressure at sea level (hPa) |

### Solar & UV Metrics
| Feature | Description |
|---|---|
| `solarradiation` | Solar radiation (W/m²) — influences mosquito activity cycles |
| `solarenergy` | Total solar energy received (MJ/m²) |
| `uvindex` | UV index — proxy for sunlight intensity |

### Target Variables
| Feature | Description |
|---|---|
| `cases` | Number of confirmed dengue cases (regression target) |
| `labels` | Risk classification — Low / Medium / High (classification target) |

---

## 🔬 Methodology

### 1. Data Preprocessing
- Handled missing values across weather attributes using median imputation
- Parsed and engineered temporal features (month, season, week of year) to capture seasonal outbreak cycles
- Normalised continuous features for distance-sensitive algorithms
- Addressed class imbalance in risk labels using appropriate weighting strategies

### 2. Exploratory Data Analysis (EDA)
- Identified seasonal dengue outbreak patterns correlating with rainy seasons and temperature peaks
- Correlation analysis revealed humidity, temperature, and precipitation as the strongest predictors of case volume
- Visualised relationships between UV index, solar radiation, and outbreak intensity
- Mapped geographic and temporal distribution of case concentrations

### 3. Feature Engineering
- Derived lag features: weather conditions from 1–3 weeks prior (to account for mosquito breeding cycle delays)
- Computed rolling averages for temperature and rainfall over 7-day and 14-day windows
- Created a composite "breeding risk index" from humidity, precipitation, and temperature interactions

### 4. Model Development

**Regression (case count forecasting):**

| Model | Purpose |
|---|---|
| Linear Regression | Interpretable baseline |
| Random Forest Regressor | Non-linear ensemble; robust feature importance |
| Gradient Boosting | High-performance boosted trees |

**Classification (risk level labelling):**

| Model | Purpose |
|---|---|
| Logistic Regression | Probabilistic baseline |
| Random Forest Classifier | Multi-class ensemble |
| Gradient Boosting Classifier | Optimised multi-class classification |

### 5. Evaluation Metrics

**Regression:** MAE, RMSE, R² Score

**Classification:** Accuracy, Precision, Recall, F1 Score (macro), Confusion Matrix

---

## 📈 Key Findings

- **Humidity and rainfall** are the strongest environmental predictors of dengue case volume — high moisture conditions directly support Aedes mosquito breeding
- **Lag features are critical** — weather conditions 1–2 weeks prior outperform same-day measurements due to the mosquito lifecycle delay
- **Seasonal peaks** align predictably with post-monsoon periods, enabling advance warning windows of 2–4 weeks
- **UV index and solar radiation** show an inverse relationship with cases — extreme heat suppresses mosquito activity

---

## 🛠️ Technologies Used

- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **Environment:** Jupyter Notebook

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/rachitkhn/Dengue-Prediction-Using-Weather-Data.git
cd Dengue-Prediction-Using-Weather-Data

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch the notebook
jupyter notebook "Dengue Case Prediction.ipynb"
```

---

## 💡 Real-World Applications

- **Early Warning Systems:** Alert health authorities 2–4 weeks in advance of predicted outbreak peaks, enabling proactive intervention
- **Resource Allocation:** Guide pre-positioning of medical supplies, fumigation teams, and healthcare capacity in high-risk periods
- **Targeted Prevention:** Focus mosquito control efforts (spraying, drainage clearing) in areas and timeframes with highest predicted risk
- **Climate & Health Research:** Quantify the relationship between climate change-driven weather shifts and dengue transmission trends

---

## 👤 Author

**Rachit Khandelwal**
[GitHub](https://github.com/rachitkhn) · [LinkedIn](https://linkedin.com/in/rachitkhn)

---

*This project was developed as part of a data science portfolio demonstrating applied ML in public health and epidemiological forecasting.*
