📌 Overview
This project presents a real-time, objective system to detect cybersickness in Virtual Reality (VR) environments using EEG brain signals. We implement a hybrid CNN-Transformer model that captures both spatial and temporal dependencies in EEG data to accurately classify cybersickness.

🎯 Goal: Eliminate reliance on subjective questionnaires and enable live detection to enhance user comfort and safety in VR.

🧪 Problem Statement
Cybersickness causes nausea, dizziness, and discomfort in VR, limiting its adoption.

Current detection methods are subjective, delayed, and non-automated.

EEG-based models often lack temporal modeling or use shallow architectures.

🚀 Solution Highlights
Real-time EEG-based detection of cybersickness.

Hybrid deep learning architecture:

CNN for spatial EEG features

Transformer for temporal pattern recognition

Preprocessing pipeline including filtering, ICA, segmentation, and feature extraction.

Achieved 98.44% accuracy and AUC-ROC: 0.9991 on test data.

🧠 Model Architecture
objectivec
Copy
Edit
Raw EEG → Preprocessing → Feature Extraction → CNN → Transformer → Fusion Layer → Classification (Sigmoid)
📦 Modules
Preprocessing Module: Filters, artifact removal, FFT, and segmentation

CNN Module: Captures spatial brain activity patterns

Transformer Module: Models temporal dependencies

Fusion Layer: Concatenates CNN + Transformer outputs

Classification Layer: Outputs cybersick/normal classification

📊 Dataset
EEG signals collected during VR experiences

Segmented into 60s windows

Time-domain + frequency-domain features (e.g., power bands, entropy)

Stored as .csv with ~154 features per sample

🔧 Technologies Used
Python

PyTorch / TensorFlow

MNE-Python, NumPy, SciPy

Matplotlib / Seaborn (for visualizations)

📈 Results
Accuracy: 98.44%

AUC-ROC: 0.9991

Balanced predictions across classes

Spectrogram & FFT visualizations show distinct neural patterns for cybersickness

📍 Future Work
Expand dataset across varied VR applications

Deploy model with wearable EEG devices

Explore multimodal fusion (e.g., motion + EEG)

📚 References
Biswas et al., ACM Computing Surveys, 2024

Jeong et al., IEEE VR, 2019

Yildirim, IEEE AIVR, 2020

Sun et al., IEEE LifeTech, 2021

Li et al., IEEE JBHI, 2021

Pahuja & Veer, Robotica, 2022
