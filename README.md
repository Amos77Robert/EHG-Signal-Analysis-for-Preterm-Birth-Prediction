# 🧠 EHG Signal Analysis for Preterm Birth Prediction

This project explores the use of electrohysterogram (EHG) signal analysis combined with machine learning to predict and interpret different types of preterm birth: **induced**, **cesarean**, or **spontaneous**. It aims to support clinical decision-making by improving signal interpretation using feature engineering and model evaluation.

---

## 📌 Table of Contents
- [Project Aim](#project-aim)
- [Objectives](#objectives)
- [Background](#background)
- [Methodology](#methodology)
- [Tools & Libraries](#tools--libraries)
- [Data Recording Protocol](#data-recording-protocol)
- [Results](#results)
- [Future Work](#future-work)
- [Data Source](#data-source)

---

## 🎯 Project Aim

To improve the prediction and interpretability of preterm physiological EHG signals for classifying birth types using machine learning.

---

## ✅ Objectives

1. Analyze preterm EHG signals from PhysioNet to identify underlying patterns.  
2. Extract and engineer features relevant to birth type classification.  
3. Train and evaluate ML models for predictive and interpretable outputs.

---

## 🧠 Background

Preterm birth—defined as delivery before 37 weeks of gestation—is a major global health challenge and the leading cause of under-five child mortality.

Malawi ranks among the highest globally in preterm birth rates, exacerbating neonatal deaths. Recent studies from the University Medical Center Ljubljana underscore the value of **surface Electrohysterograph (EHG) signals** as a non-invasive technique for early prediction.

This project utilizes the Ljubljana dataset to extract diagnostic features from abdominal EHG signals, addressing the clinical interpretability gap through signal decomposition, feature engineering, and predictive modeling.

---

## 🔬 Methodology

1. **Signal Preprocessing**
   - Wavelet decomposition for noise reduction and pattern isolation.

2. **Frequency Analysis**
   - Fast Fourier Transform (FFT) for dominant component identification.
   - Welch’s method for Power Spectral Density estimation.

3. **Feature Extraction**
   - Time and frequency domain features using wavelet scattering transform.

4. **Feature Engineering**
   - Normalization and feature selection.

5. **Machine Learning**
   - Trained initial model using Random Forest classifier.
   - Evaluation through confusion matrices and performance metrics.

---

## 🛠️ Tools & Libraries

### 🧪 Tools
- Python  
- Jupyter Notebook

### 📚 Libraries
- [WFDB](https://wfdb.readthedocs.io/en/latest/): Reading physiological signals  
- [Wavelet Scattering](https://www.mathworks.com/help/wavelet/ug/wavelet-scattering.html): Feature transformation  
- [Welch Method](https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.welch.html): Spectral density  
- [FFT](https://docs.scipy.org/doc/scipy/reference/generated/scipy.fft.fft.html): Frequency analysis  

---

## 🧾 Data Recording Protocol

Data was collected using **four Ag₂Cl electrodes** placed symmetrically above and below the navel (7 cm apart):

<div align="center">
    <img src="https://github.com/Amos77Robert/Electrohysterograph-EHG-for-Preterm-Birth-Signal-Analysis/blob/main/data/Figure_1.jpg" alt="EHG Electrode Placement" width="300">
    <p><b>Fig 1: Electrode placement on the lower abdomen</b></p>
</div>

- **Signal Length**: ~30 minutes  
- **Channels**: 3 bipolar signals  
- **Sampling Rate**: 20 Hz  
- **Filter**: Analog low-pass Butterworth, cutoff = 5 Hz  
- **Resolution**: 16-bit, ±2.5 mV range (1.0 mV = 13,107 A/D units)

---

## 📊 Results

**Model Tested**: Random Forest Classifier  
- **Input**: Extracted features from decomposed EHG signals  
- **Output**: Birth type classification  

<div align="center">
  <img src="https://github.com/Amos77Robert/EHG-Signal-Analysis-for-Preterm-Birth-Prediction/blob/main/experiments/results/Trained%20ML%20models/Random%20Forest%20Performance%20metrics.PNG?raw=true" alt="Random Forest Performance" width="600"/>
  <p><b>Fig 2: Random Forest Performance Metrics</b></p>
</div>

---

## 🔁 Future Work

- Apply **PCA (Principal Component Analysis)** to enhance feature selection and reduce noise.  
- Experiment with additional models including logistic regression, SVMs, and ensemble techniques.  
- Optimize hyperparameters and test generalization on new test sets.

---

## 🧬 Data Source

**Jager, F. (2023)**  
*Induced Cesarean EHG DataSet (ICEHG DS): An open dataset with electrohysterogram records of pregnancies ending in induced and cesarean section delivery.*  
📥 [PhysioNet DOI](https://doi.org/10.13026/zw34-n382)

---
