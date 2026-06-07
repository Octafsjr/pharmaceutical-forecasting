# Pharmaceutical Forecasting using Classical and Deep Learning Models

## 📄 Abstract

This study investigates the forecasting of pharmaceutical deviation occurrences using both classical statistical models and deep learning approaches. The main objective is to compare the predictive performance of Holt-Winters, ARIMA, and SARIMA models against neural network-based architectures, including Multilayer Perceptron (MLP), Recurrent Neural Network (RNN), and Gated Recurrent Unit (GRU).

The models were evaluated using multiple error metrics, including RMSE, MAPE (normalized and real scale), sMAPE, MASE, Theil’s inequality coefficient, and R², under a consistent experimental framework. All models were trained and tested on the same time series data representing weekly counts of pharmaceutical deviations.

The results indicate that neural network models generally outperform classical statistical approaches in capturing nonlinear temporal patterns. The MLP model showed the most consistent performance across evaluation metrics, while the RNN achieved strong point forecasting accuracy. The GRU model did not significantly outperform simpler architectures, which may be explained by the limited long-term temporal dependencies in the dataset, with significant autocorrelation concentrated within approximately 16 lags.

Overall, the findings highlight the importance of selecting forecasting models based on the underlying temporal structure of the data, rather than model complexity alone.

## 🔑 Keywords

Pharmaceutical forecasting; Time series analysis; Deep learning; ARIMA; SARIMA; MLP; RNN; GRU; Forecasting models; Machine learning

## ⭐ Highlights

- Comparison between classical statistical and deep learning forecasting models
- Evaluation of Holt-Winters, ARIMA, SARIMA, MLP, RNN, and GRU models
- Neural networks outperform classical models in nonlinear pattern learning
- MLP shows the most stable performance across multiple error metrics
- Limited temporal memory (~16 lags) explains GRU performance behavior

## 📌 Project Overview

This project investigates the forecasting of pharmaceutical deviation occurrences using both classical statistical models and deep learning approaches. The goal is to compare predictive performance across different methodologies and evaluate their ability to capture temporal patterns in the data.

The models implemented include:
- Holt-Winters (HW)
- ARIMA
- SARIMA
- Multilayer Perceptron (MLP)
- Recurrent Neural Network (RNN)
- Gated Recurrent Unit (GRU)

Multiple error metrics are used to ensure a robust and comprehensive evaluation of forecasting performance.

---

## 📊 Dataset Description

The dataset consists of a time series representing weekly counts of pharmaceutical deviations. The series exhibits non-stationary behavior and potential seasonal patterns, requiring both statistical transformations and advanced modeling techniques.

---

## 🧠 Methodology

### Classical Models
- Holt-Winters: captures trend and seasonality
- ARIMA: models autoregressive and moving average components
- SARIMA: extends ARIMA with seasonal structure

### Deep Learning Models
- MLP: feedforward neural network using lagged observations
- RNN: recurrent architecture for sequential dependency modeling
- GRU: gated recurrent network for long-term dependency learning

---

## 📐 Evaluation Metrics

The following metrics were used to evaluate model performance:

- RMSE (Root Mean Squared Error)
- MAPE$_N$ (Normalized Mean Absolute Percentage Error)
- MAPE$_R$ (Real-scale Mean Absolute Percentage Error)
- sMAPE (Symmetric MAPE)
- MASE (Mean Absolute Scaled Error)
- Theil’s U inequality coefficient
- R² (Coefficient of Determination)

---

## 📈 Key Findings

- Neural network models generally outperform classical statistical models in capturing nonlinear patterns.
- MLP demonstrated strong and consistent performance across multiple metrics.
- RNN achieved competitive RMSE and R² but showed less stability in percentage-based metrics.
- GRU did not significantly outperform simpler architectures, likely due to limited long-term dependencies in the dataset (≈16 lags of relevant autocorrelation).
- Classical models performed well in structured seasonal behavior but were less robust to nonlinear dynamics.

---

## 🧪 Reproducibility

To ensure reproducibility, all models were trained using fixed random seeds across frameworks (NumPy, TensorFlow, and Python random).

---

## 📁 Repository Structure

Pharmaceutical_forecasting/
│
├── Classical Models/
├── Models/
├── Statistical Analysis
└── README.md


---

## ⚙️ Requirements

Main dependencies:

- Python 3.9+
- NumPy
- Pandas
- Matplotlib
- Statsmodels
- Scikit-learn
- TensorFlow

---

## 🚀 How to Run

Example (for notebooks):

1. Open Jupyter Notebook
2. Run classical models first (ARIMA/SARIMA/HW)
3. Run neural network models (MLP/RNN/GRU)
4. Compare results using evaluation metrics

---

## 📌 Authors

- Master’s Student (Pharmaceutical Forecasting Study)
- Academic Supervisor

---

## 📄 License

This project is intended for academic and research purposes.
