# Pharmaceutical Forecasting using Classical and Deep Learning Models

## 📄 Abstract

This study investigates the forecasting of pharmaceutical quality deviation occurrences using classical statistical models and artificial neural network-based approaches. The main objective is to compare the predictive performance of Holt-Winters, ARIMA, and SARIMA models against neural network architectures, including Multilayer Perceptron (MLP), Recurrent Neural Network (RNN), and Gated Recurrent Unit (GRU).

The models were evaluated using a real-world pharmaceutical manufacturing dataset collected from a GMP-regulated environment. A consistent experimental framework was adopted, using the same training and testing conditions for all approaches. Forecasting performance was assessed using multiple error metrics, including RMSE, MAE, MAPE, sMAPE, MASE, Theil’s inequality coefficient, and R².

Neural network models were trained using an 11-lag sliding window, optimized through random search, and evaluated over ten independent executions to account for stochastic variations during training. Statistical validation was performed using walk-forward evaluation, Friedman tests, and post-hoc comparisons using Conover and Wilcoxon tests with Holm correction.

The results demonstrate that neural network-based models consistently outperform classical statistical approaches in forecasting pharmaceutical deviations. The RNN model achieved the best overall numerical performance, reducing RMSE by approximately 58.2% compared with the best classical benchmark (SARIMA). However, statistical analyses indicated no significant differences among MLP, RNN, and GRU in most comparisons, suggesting that model selection should also consider computational complexity and implementation requirements.

Overall, the findings highlight the potential of data-driven forecasting approaches as decision-support tools for proactive pharmaceutical quality management.

## 🔑 Keywords

Pharmaceutical forecasting; Time series analysis; Deep learning; ARIMA; SARIMA; MLP; RNN; GRU; Forecasting models; Machine learning

## ⭐ Highlights

Comparison between classical statistical and neural network forecasting approaches
Evaluation of Holt-Winters, ARIMA, SARIMA, MLP, RNN, and GRU models
Real GMP pharmaceutical manufacturing data used for weekly deviation forecasting
RNN reduces RMSE by 58.2% compared with the best classical forecasting model
Statistical tests confirm significant advantages of neural approaches over classical models

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

The dataset consists of weekly pharmaceutical quality deviation records collected between 2018 and 2025 from a GMP-regulated manufacturing environment.

Dataset characteristics:

Frequency: Weekly
Observations: 400 weeks
Target variable: Number of quality deviations per week
Seasonal period: 53 weeks

Due to confidentiality agreements with the industrial partner, the original dataset cannot be publicly shared. The repository contains the complete analytical workflow and implementation used in the study.

---

## 🧠 Methodology

### Classical Models
Holt-Winters (HW)
Models trend and seasonal components using exponential smoothing
Suitable for structured temporal patterns
ARIMA
Captures autoregressive behavior, differencing, and moving-average components
Final configuration:
ARIMA(4,1,5)
SARIMA
Extends ARIMA by incorporating seasonal dependencies
Final configuration:
SARIMA(4,1,5)(0,1,1)53

### Deep Learning Models
Multilayer Perceptron (MLP)
Feedforward neural network
Uses lagged observations as input features
Captures nonlinear relationships

Recurrent Neural Network (RNN)
Sequential architecture with recurrent memory states
Designed for temporal dependency modeling

Gated Recurrent Unit (GRU)
Recurrent architecture using gating mechanisms
Designed to capture longer temporal dependencies with reduced complexity

Neural network models were trained using:

11-lag sliding window input representation
Random search hyperparameter optimization
20% validation split
10 independent training executions

---

## 📐 Evaluation Metrics

The forecasting performance was evaluated using multiple complementary metrics:

RMSE (Root Mean Squared Error)
MAE (Mean Absolute Error)
MAPE (Mean Absolute Percentage Error)
sMAPE (Symmetric Mean Absolute Percentage Error)
MASE (Mean Absolute Scaled Error)
Theil’s U inequality coefficient
R² (Coefficient of Determination)

Statistical analyses included:

Friedman test
Conover post-hoc test with Holm correction
Wilcoxon signed-rank test with Holm correction

A walk-forward evaluation strategy was also applied to verify model behavior under sequential forecasting conditions.

---

## 📈 Key Findings

Neural network-based models consistently outperform classical statistical forecasting methods.
The RNN achieved the best numerical forecasting performance among all evaluated approaches.
Compared with SARIMA, the best classical model, RNN reduced RMSE from 2.092 to 0.875 (approximately 58.2% improvement).
Classical models successfully captured trend and seasonal components but showed limitations in representing nonlinear variations.
MLP, RNN, and GRU achieved comparable performance in most statistical comparisons.
Model selection should consider not only accuracy but also computational cost and implementation requirements.

---

## 🧪 Reproducibility

To improve reproducibility:

All models were evaluated using the same train/test split:
70% training
30% testing
Neural network models were evaluated over:
10 independent executions
Hyperparameter optimization was performed using:
Random search strategy
Statistical validation was performed using:
Walk-forward evaluation
Non-parametric statistical tests

---

## 📁 Repository Structure

Pharmaceutical_forecasting/ 
│ 
├── Classical Models/ 
│ ├── Holt-Winters 
│ ├── ARIMA 
│ └── SARIMA 
│ 
├── Neural Network Models/ 
│ ├── MLP 
│ ├── RNN 
│ └── GRU 
│ 
├── Statistical Analysis/ 
│ ├── Evaluation metrics 
│ ├── Friedman test 
│ ├── Conover test 
│ └── Wilcoxon test  
│ 
└── README.md


---

## ⚙️ Requirements

Main dependencies:

Python 3.9+
NumPy
Pandas
Matplotlib
Seaborn
Statsmodels
Scikit-learn
TensorFlow
Keras

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
