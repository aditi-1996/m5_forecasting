# Explainable M5 Accuracy Forecasting

This work includes creating of time series models on [M5 Forecasting - Accuracy](https://www.kaggle.com/competitions/m5-forecasting-accuracy) and explaining its prediction usinh [WIT](https://pair-code.github.io/what-if-tool/) tool.

# Directory Structure

```bash
xai_m5_forecasting/
├── notebooks
│   ├── M5_counterfactual_analysis_daily_wit.ipynb
│   ├── m5-time-series-forecasting-data-eda.ipynb
│   ├── m5-time-series-modelling-ca-only.ipynb
│   ├── m5-time-series-modelling-combined-1-day.ipynb
│   └── m5-time-series-modelling-combined-28-day.ipynb
├── README.md
└── weights
    ├── M5_LSTM_CA.h5
    ├── M5_LSTM_CA_TX_WI_28_days.h5
    └── M5_LSTM_CA_TX_WI.h5
```

# Environment Setup

1. Create virtual environment: `python3 -m venv m5_forecasting`

2. Activate virtual environemnt: `source m5_forecasting/bin/activate`

3. Install packages: `python3 -m pip install -r requirements.txt`


## Notebooks Definition

- `m5-time-series-forecasting-data-eda.ipynb`: Contains code for EDA of data.
- `m5-time-series-modelling-ca-only.ipynb` : Contains code for time series modelling for California state only.
- `m5-time-series-modelling-combined-1-day.ipynb`: Contains code for time series modelling for all states (CA, TX, WI) combined and forecasting for 1 day given past 28 days.
- `m5-time-series-modelling-combined-28-day.ipynb`: Contains code for time series modelling for all states (CA, TX, WI) combined and forecasting for 28 day given past 28 days.
- `M5_counterfactual_analysis_daily_wit.ipynb`: Contains code for performing counterfactual analysis using WIT tool.

## Weights Definition

- `M5_LSTM_CA.h5`: Weight file for LSTM model for Californial only.
- `M5_LSTM_CA_TX_WI.h5`: Weight file for LSTM model for all states combined and having prediction for 1 day in future given past 28 days.
- `M5_LSTM_CA_TX_WI_28_days.h5`: Weight file for LSTM model for all states combined and having prediction for 28 day in future given past 28 days.

## NOTE

- `M5_counterfactual_analysis_daily_wit.ipynb` has been tested in local environment using Anaconda. 

## Future Steps:

- Include [`SHAP`](https://shap.readthedocs.io/en/latest/) analysis.

## Contributing Guidelines

- Feel free to open PR for ineteresting findings.

## Acknowledgements

- https://www.kaggle.com/code/jestelrod/m5-eda-plotly-lstm-neural-network-vs-xgboost
- https://github.com/KunalArora/kaggle-m5-forecasting


