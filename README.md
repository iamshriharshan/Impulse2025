# EEG Seizure Classification - Impulse 2025

There are 2 notebooks, Notebook-2 has the final model. Notebook-1 contains some visualizations and first attempt I took to train the model(which isn't soo good) 

## Overview
This notebook outlines the approach for classifying EEG seizure types as part of the Impulse 2025 hackathon. The tasks included:
1. Preprocessing and denoising EEG signals.
2. Extracting time-domain and frequency-domain features.
3. Building and evaluating classification models.
4. Implementing interpretability techniques.

## Approach
### 1. Data Preprocessing
- Loaded EEG signals from `.npy` files for all classes.
- Reshaped data for compatibility with models like LSTM.

### 2. Denoising
- Trained an LSTM-based autoencoder to remove noise.
- Evaluated denoised signals using PSNR and visualizations.

### 3. Feature Extraction
- Extracted features like mean, variance, RMS (time domain).
- Used Fourier Transform and Wavelet Decomposition (frequency domain).

### 4. Model Development
- Built an SVM as the baseline model.
- Trained an LSTM for the final model, achieving high performance on validation data.

## Results
- **Final Model**: Bi-directional LSTM
- **ROC-AUC**: 49.46%
- **Balanced Accuracy**: 54.75%

## Test Predictions
Predictions are saved in `test_outputs.csv`.



