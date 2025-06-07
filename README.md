# EHG signal analysis for preterm birth prediction
# Aim
To improve the prediction and interpretability of preterm physiological EHG signals for identifying birth types (induced, cesarean, or spontaneous) using machine learning.

# Objectives
1. Analyze preterm EHG signals from physionet.org to understand key patterns
2. Extract and engineer features relevant for birth type prediction
3. Develop and evaluate machine learning models to predict and interpret preterm birth types
   
# Background
This project addresses the global challenge of preterm births, a leading cause of under-five child mortality worldwide. Preterm birth refers to babies born before 37 weeks of pregnancy, with varying degrees of prematurity.

Malawi has one of the highest preterm birth rates globally, contributing significantly to neonatal deaths. Recent research from the University Medical Center Ljubljana highlights surface Electrohysterograph (EHG) signals as a promising non-invasive tool for automated preterm birth prediction.

This project focuses on improving the interpretation of EHG signals, which remains challenging for health workers, by developing a machine learning model using the preterm physiological dataset from Ljubljana to aid clinical decision-making.

# Methodology
1). EHG signal decomposition using wavelet transforms  
2). Data analysis:  
            . Frequency component analysis using digital Fast Fourier Transform  
            . Power Spectral Density analysis using Welch method    
3). Feature extraction in frequency and time domains using scattering algorithm    
4). Feature engineering  
5). Experiment with ML model 
# Tools
Python, Jupyter Notebook
# Libraries 
1). [WFDB](https://wfdb.readthedocs.io/en/latest/)  
2). [Wevelet Scattering algorithm](https://www.mathworks.com/help/wavelet/ug/wavelet-scattering.html)  
3). [Welch method](https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.welch.html)  
4). [Fast Fourier Transform](https://docs.scipy.org/doc/scipy/reference/generated/scipy.fft.fft.html)  
# Data recording protocol from the source(Jager and F, 2023)  
The records were collected from the abdominal surface using four Ag2Cl electrodes. The electrodes were placed symmetrically above and under the navel, at the distance of 7 cm (see Fig 1).    
<div align="center">
    <img src="https://github.com/Amos77Robert/Electrohysterograph-EHG-for-Preterm-Birth-Signal-Analysis/blob/main/data/Figure_1.jpg" alt="Image Title" width="300">
    <p><b>Fig 1: Showing surface electrodes on the lower abdomen</b></p>
</div>
The acquired EHG records are of length of approximately 30 minutes and consist of three bipolar EHG signals. The first acquired bipolar EHG signal was measured between the upper two electrodes, S1 = E2 - E1, the second bipolar EHG signal between the left two electrodes, S2 = E2 - E3, and the third bipolar EHG signal between the lower two electrodes, S3 = E4 - E3. Prior to sampling, the signals were filtered using an analog anti-aliasing low pass three-pole Butterworth filter with the cutt-off frequency of 5.0 Hz. The sampling frequency, Fs, was 20 Hz. 
The resolution of the signal acquisition equipment was 16 bits with the amplitude range of ±2.5 mV (A/D value of 13107 units corresponds to 1.0 mV).  

# Results of model training
- Model Tested: Random Forest
![Random Forest Performance Metrics](https://github.com/Amos77Robert/EHG-Signal-Analysis-for-Preterm-Birth-Prediction/blob/main/experiments/results/Trained%20ML%20models/Random%20Forest%20Performance%20metrics.PNG?raw=true)

## Improvement plans
- To use PCA technique to filter features and retrain the models again
- Train on other models such as regression models
  
# DATA SOURCE:  
Jager, F. (2023). Induced Cesarean EHG DataSet (ICEHG DS): An open dataset with electrohysterogram records of pregnancies ending in induced and cesarean section delivery (version 1.0.1). PhysioNet. https://doi.org/10.13026/zw34-n382.


