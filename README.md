# Electrohysterograph (EHG) for Preterm Birth Signal Analysis
Exploratory and experimental 
# Scope
Mini
# Aim
Seeks to improve interpretability of the recorded preterm physiological EHG signals from pregnant mothers by understanding signal mechanisms which lead to induced and cesarean births.
# Objectives
1). Analyse signals obtained from physionet.org for preterm birth  
2). Extract features and perform feature engineering   
3). Experiment with various computational methods to predict preterm birth type
# Disclaimer
This is a personal project driven by curiosity and interest to apply computational intelligence to better understand nature. It is being conducted during weekends.
# Description
It focuses on tackling the global challenge of preterm births. According to the WHO article from 2023, an estimated 13.4 million babies were born preterm in 2020. The article highlights that complications from preterm birth are the leading cause of death among children under five, accounting for 900,000 deaths worldwide in 2019.

Preterm is defined as babies born alive before 37 weeks of pregnancy are completed. Sub-categories include: extremely preterm (less than 28 weeks), very preterm (28 to less than 32 weeks) and moderate to late preterm (32 to 37 weeks).

In Malawi, UNICEF reported that prematurity was responsible for 33% of neonatal deaths in 2015. In 2020, the National Institutes of Health reported that Malawi has the highest rate of preterm births globally, with rates up to 29.7%.

A recent study at the University Medical Center Ljubljana in Slovenia identifies surface EHG as a promising diagnostic tool for non-invasive automated preterm birth prediction(Jager and F, 2023). This small scale project specifically tries to address difficulties in interpreting EHG signals faced by health workers. I will utilize the preterm physiological dataset created at University Medical Center in Slovenia. A machine learning model will be developed to aid in interpretability of the EHG signals in clinical setting.
# Methodology
1). EHG signal decomposition using wavelet transforms  
2). Data analysis:  
            . Frequency component analysis using digital Fast Fourier Transform  
            . Power Spectral Density analysis using Welch method    
3). Feature extraction in frequency and time domains using scattering algorithm    
4). Feature engineering  
5). Experiment with ML models  
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

# Expected outcomes
1). Valuable analytical insights      
2). Feature dataset      
3). Trained machine learning models  
# DATA SOURCE:  
Jager, F. (2023). Induced Cesarean EHG DataSet (ICEHG DS): An open dataset with electrohysterogram records of pregnancies ending in induced and cesarean section delivery (version 1.0.1). PhysioNet. https://doi.org/10.13026/zw34-n382.


