## Project Overview

This project replicates and extends Nunn (2008), *The Long-Term Effects of Africa's Slave Trades*. The original paper examines the long-term relationship between historical slave exports and modern economic development in African countries.

The machine-learning extension applies Double Machine Learning (DML) to the original OLS and instrumental-variable specifications. Machine-learning methods are used to estimate the nuisance functions, while the original causal identification strategy is preserved.
## Run the Analysis

The complete analysis can be opened and executed in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1MpYdzEj6YVaBt0oOsKeu1QoKJ9J__1-W?usp=sharing)

## Research Question

Can Double Machine Learning improve the estimation of the relationship between historical slave exports and modern income by allowing more flexible relationships between the outcome, treatment, instruments, and control variables?

## Original Empirical Approach

The original paper estimates the relationship between historical slave exports and modern economic development using:

- Ordinary Least Squares (OLS)
- Instrumental Variables / Two-Stage Least Squares (IV/2SLS)
- Historical minimum distances to slave demand markets as instruments

## Machine-Learning Extension

The extension applies Double Machine Learning to both the OLS and IV settings.

The analysis includes:

- Ten machine-learning learners, including linear and nonlinear learners
- Five-fold cross-fitting
- Repeated 500 splitting
- Comparison of coefficients, standard errors, and statistical significance

The machine-learning methods are used only to estimate the nuisance functions. The final causal parameter is estimated using the original strategy.


## Repository Structure

Nunn-2008-DML-extension/
│
├── README.md
├── data/
│   └── slave_trade_QJE.dta
├── ML_extension_Nunn_(2008).ipynb
├── Guo_Jiani_ExtensionReport.pdf
├── Guo_Jiani_ExtensionPoster.pdf
├── AI_DISCLOSURE.md
├── figures/
├── tables/
└── .gitignore
