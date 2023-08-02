# PPG-BP-Project
Extracting estimation to blood pressure change in anesthetized patient based on PPG signal

# Introduction
Blood pressure (BP) monitoring is essential for detecting complications during surgeries. Current methods include invasive catheters and non-invasive cuffs. However, invasiveness poses infection and bleeding risks, while non-invasiveness causes discomfort and lacks continuous monitoring. The project collaborates with Nervio, a digital health startup using AI for real-time neurological monitoring.

# Project goal
Investigate methods for continuous non-invasively detecting BP using a single PPG sensor to be used during surgery under anesthesia.

# Data
The project based on PPG signal and BP from 67 sedated cervical spine surgery patients at Belinson Hospital. PPG sensor measures at 100 Hz, detecting blood volume changes. BP collected invasively one measurement per minute on average (~1/60 Hz), and non-invasive at irregular rate.

# Methodology
This study aims to develop a machine learning model to estimate changes in MAP value using features of the PPG waveform. The steps to achieve the goal include performing extensive pre-processing on the PPG signals received from the company, removing noise and various artifacts from the waves and extracting relevant characteristics correlated to the target variable, a change in MAP. Finally, entering the data into guided models of various types, performing an adjustment of the hyperparameters and obtaining the prediction results. Depending on the results obtained, the expansion of the processes and the addition of various parameters to improve the model's ability to learn and predict. This process was performed based on various articles investigating the ability to predict BPs based on a single PPG sensor. However, no articles were found that succeeded in this task in a way that meets the AAMI guidelines. Also, most of the reviewed articles do not use a data set similar to the project data, which includes a variety of patient data under the influence of anesthesia.

# Conclusions
Based on the results of the study, an SVM regression model yielded the best favorable results for accurate BP prediction. Additionally, it been found that taking a BP at the beginning of the surgeries and using it as a Baseline feature serves as calibration, significantly enhancing the model's predictions.

# Discussions
The developed algorithm shows potential for a BP prediction system using a single PPG sensor. Further research is needed for additional waveform features. Sophisticated methods for BP categories and continuous prediction via deep learning should be explored. Evaluating on an extended dataset with over 85 patients could meet AAMI standards. PPG-based devices may greatly impact patient monitoring, especially for those at risk of cardiovascular diseases, requiring continuous monitoring.

***
