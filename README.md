# Deep-Learning-Final-Project---S&P 500-Prediction

# Time Series Forecasting: Index 2018 Dataset  
This project compares **classical statistical models** and **deep learning architectures** for time series forecasting using the *Index 2018 dataset*.  
The goal is to evaluate how traditional approaches such as **ARIMA** perform relative to modern sequence models such as **LSTM**, **GRU**, and **Transformers**.

## Project Overview
The repository contains multiple notebooks that walk through the full workflow:

### ** Data Preparation & EDA**
- Loading and cleaning the Index 2018 dataset  
- Handling missing values  
- Time-series visualization and decomposition  
- Train/validation/test split using chronological order  

---

## Models Implemented

### ARIMA (Classical Statistical Model)
- Full differencing and stationarity checks  
- ACF/PACF analysis  
- Model fitting and residual diagnostics  
- Baseline performance metric

### LSTM (Long Short-Term Memory)
- Sequence windowing  
- Multi-layer LSTM architecture  
- Dropout regularization  
- Adam optimization  
- Performance measured on predictions vs. actual values  

### GRU (Gated Recurrent Unit)
- GRU-based sequential model  
- Tuned hidden units and learning rate  
- Faster training vs. LSTM with comparable accuracy  

### Transformer Model
- Encoder-only time-series forecasting transformer  
- Multi-head attention layers  
- Positional embeddings  
- Trained using MSE loss & AdamW  
- Best performance among deep learning models (typically)  


## Evaluation Metrics
All models were compared using:

- **MAE – Mean Absolute Error**  
- **RMSE – Root Mean Squared Error**  
- **R² Score** (where applicable)  
- **Visual analysis of prediction curves**


## Key Findings
- **ARIMA** provided a reasonable statistical baseline, performing surprisingly well given its simplicity, but it struggled to adapt to rapid market fluctuations and long-term trend shifts. 
- **LSTM and GRU** outperformed all other models, offering the closest alignment with the actual S&P 500 trend. Their ability to capture sequential patterns and short-term dependencies allowed them to generate stable, accurate rolling forecasts. 
- **Transformer** Despite being a powerful architecture for many sequence tasks, it underperformed here — producing smoother, less responsive predictions and failing to track local variations in the index. This is consistent with the fact that Transformers typically require large datasets and extensive tuning to outperform RNN-based models in time series forecasting.
- Overall, deep learning models (LSTM, GRU) delivered the best accuracy, while ARIMA performed adequately but more conservatively. The Transformer model lagged behind due to underfitting and weaker short-term predictive precision.




