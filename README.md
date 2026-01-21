# WiFi Sensing–Based Human Activity Recognition using Machine Learning and Deep Learning

## 📌 Overview
This project presents a **device-free and privacy-preserving Human Activity Recognition (HAR) system** using **WiFi Channel State Information (CSI)**.  
Unlike camera-based or wearable sensor–based systems, WiFi sensing detects human activities by analyzing variations in wireless signals caused by human movement.

The proposed framework combines **classical machine learning** and **deep learning** approaches to recognize human activities from WiFi CSI data.

---

## 🎯 Motivation
Traditional HAR systems suffer from:
- **Privacy concerns** (camera-based systems)
- **User inconvenience** (wearable sensors)
- **Limited usability in dark or occluded environments**

WiFi sensing overcomes these issues by:
- Working **without cameras or body-worn devices**
- Using **existing WiFi infrastructure**
- Preserving user **privacy**
- Enabling **continuous and contactless monitoring**

---

## 🛠 Methodology

### 1. Data Processing
- Raw WiFi CSI signals are segmented into **fixed-length sliding windows**
- Each window represents one activity instance

### 2. Classical Machine Learning Pipeline
- **Statistical features** (mean, variance, energy, etc.) are extracted from CSI windows
- A **Random Forest classifier** is trained using these handcrafted features

### 3. Deep Learning Pipeline
- CSI windows are transformed into **time–frequency representations**
- These representations are resized into **32×32 grayscale images**
- A **Convolutional Neural Network (CNN)** is trained for activity classification

---

## 🧠 Models Used
- **Random Forest** (for statistical feature-based classification)
- **Convolutional Neural Network (CNN)** (for spectrogram-based deep learning)

---

## 📊 Results
- CNN trained on the custom WiFi CSI dataset achieved **~93% test accuracy**
- Random Forest achieved very high accuracy using handcrafted features
- **Cross-dataset evaluation** was performed by testing the trained CNN on a public dataset without retraining
- Cross-dataset accuracy dropped, highlighting **real-world generalization challenges**

---

## 🔍 Cross-Dataset Evaluation
- Evaluated the trained CNN on a **public benchmark dataset**
- No fine-tuning or retraining was performed
- Demonstrates the difficulty of generalizing WiFi sensing models across:
  - Different environments
  - Different sensors
  - Different data distributions

---

## 🚀 Key Contributions
- Device-free WiFi CSI–based activity recognition framework
- Comparison of **machine learning vs deep learning approaches**
- Conversion of CSI signals into CNN-compatible image representations
- Cross-dataset validation to assess real-world robustness
- Privacy-preserving alternative to camera-based HAR systems

---

## 🔮 Future Work
- Collect and evaluate a **new WiFi CSI dataset**
- Perform extensive **cross-environment and cross-dataset evaluation**
- Explore additional deep learning architectures
- Investigate **domain adaptation and feature alignment techniques**
- Reduce performance degradation in cross-dataset scenarios

---

## 🧪 Technologies Used
- Python
- NumPy, SciPy
- Scikit-learn
- TensorFlow / Keras or PyTorch
- Signal Processing (STFT, Time–Frequency Analysis)

---

## 📂 Project Structure

├── data/ # WiFi CSI datasets
├── preprocessing/ # CSI cleaning and windowing
├── feature_extraction/ # Statistical feature computation
├── models/
│ ├── random_forest.py
│ └── cnn_model.py
├── evaluation/ # Metrics and reports
├── results/ # Accuracy and plots
├── README.md
└── requirements.txt

---

## 📌 Keywords
WiFi Sensing, Channel State Information, Human Activity Recognition,  
Convolutional Neural Network, Random Forest, Time-Frequency Analysis,  
Cross-Dataset Evaluation

---

## 👩‍💻 Author
**Shilpi Rani**  
University of Hyderabad  

---

## 📜 License
This project is for academic and research purposes.
