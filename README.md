# Spectral Winds of Bitcoin 📈⚡
### A Frequency-Domain Analysis of BTC Predictability Using FFT and Wavelet Features

> *"Prediction is very difficult, especially if it's about the future."*  
> — Niels Bohr

---

## Overview

Financial markets are notoriously difficult to predict, particularly
in the short term. Bitcoin (BTC), known for its extreme volatility,
presents an interesting challenge for quantitative modeling.

This project investigates whether **frequency-domain methods**
can extract predictive structure from financial time series.

Specifically, we compare:

- **Fast Fourier Transform (FFT)** — global frequency analysis
- **Wavelet Transform** — localized time-frequency analysis

The goal is to determine whether these spectral methods
can provide useful features for predicting **next-day BTC returns**.

---

## Objectives

The main research questions are:

1. Can frequency-domain representations improve short-term prediction?
2. Do wavelets outperform FFT in non-stationary financial data?
3. Can these methods outperform naive baseline models?

Success is evaluated using:

- **Regression:** MAE and RMSE vs baseline
- **Classification:** Accuracy and ROC AUC vs random guess

---

## Contents

| File | Description |
|------|-------------|
| `BTC_FFT_vs_Wavelet_Predictability.ipynb` | Main analysis notebook |
| `README.md` | Project documentation |

---

## Methods

This project combines **signal processing**, **machine learning**,  
and **statistical evaluation**.

### Feature Extraction

- **FFT (Fast Fourier Transform)**
  - Extracts dominant frequency components
  - Uses magnitude of first K coefficients

- **Wavelet Transform (Morlet Wavelet)**
  - Captures localized time-frequency behavior
  - Handles non-stationary signals

### Data Processing

- BTC-USD daily data from **Yahoo Finance**
- Log returns used instead of prices
- Rolling window feature construction

### Models

- **Ridge Regression**
- **Logistic Regression**

These models are intentionally simple to isolate the effect
of feature representations.

---

## Dataset

- Asset: **BTC-USD**
- Source: Yahoo Finance (`yfinance`)
- Frequency: Daily
- Start Date: January 1, 2014
- Target Variable: Next-day log return

Data preparation includes:

- Log return computation
- Rolling window segmentation
- Chronological train/test split (70/30)

---

## Key Results

Typical findings from the analysis:

- Both FFT and Wavelet features provide
  measurable structure beyond naive baselines.
- Wavelets generally perform slightly better
  in non-stationary regimes.
- Overall predictability remains limited,
  consistent with known properties
  of financial markets.

These results confirm that:

**Short-term financial prediction remains inherently difficult,
but spectral methods provide useful analytical insight.**

---

## Visualizations

The notebook includes:

- Price and return plots
- FFT spectrum visualization
- Wavelet coefficient heatmaps
- Prediction vs realization plots
- Cumulative comparison curves
- Statistical performance metrics

---

## Limitations

This project intentionally simplifies several aspects:

- Single chronological train/test split
- No transaction costs
- Linear models only
- No hyperparameter optimization

Financial markets are highly complex, and
results should be interpreted cautiously.

---

## Requirements

Python 3 (Anaconda recommended)

Required libraries:
