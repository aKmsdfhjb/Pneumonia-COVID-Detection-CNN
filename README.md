

# 🩻 [Pneumonia-COVID-Detection-CNN]

**A Deep Learning Web Application for Automated Detection of COVID-19 and Pneumonia from Chest X-Rays.**

## 📌 Overview

This project provides a rapid screening tool for respiratory infections. It utilizes a **Convolutional Neural Network (CNN)** trained on a multi-class dataset to distinguish between **Normal** lungs, **Viral Pneumonia**, and **COVID-19** infections from Posterior-Anterior (PA) chest X-ray images.

### Key Features

* **Multi-Class Classification:** Specifically tuned to distinguish COVID-19 from standard viral pneumonia.
* **Interactive Frontend:** Easy-to-use web interface for medical professionals to upload and analyze scans.
* **High Sensitivity:** Optimized for **Recall** to minimize dangerous False Negatives in a clinical context.
* **Performance Visualization:** Includes Confusion Matrices and Training Logs for transparency.

---

## 🏗️ Technical Architecture

The model is built using a custom **Sequential CNN** architecture with the following layers:

1. **Convolutional Blocks:** Feature extraction with ReLU activation.
2. **Batch Normalization:** Ensuring stable training across varying X-ray exposures.
3. **Global Average Pooling:** Reducing parameters and preventing overfitting.
4. **Softmax Output:** Generating probability scores for all three classes.

---

## 📊 Performance Metrics

The model was evaluated using a test set containing balanced samples of all three categories.

| Class | Precision | Recall | F1-Score |
| --- | --- | --- | --- |
| **Normal** | 0.94 | 0.96 | 0.95 |
| **Pneumonia** | 0.91 | 0.89 | 0.90 |
| **COVID-19** | 0.97 | 0.98 | 0.97 |

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/aKmsdfhjb/Pneumonia-COVID-Detection-CNN.git
cd PulmoScan-AI

```

### 2. Install dependencies

```bash
pip install -r requirements.txt

```

### 3. Run the application

```bash
streamlit run app.py

```

---

## 📂 Dataset

The model was trained using 
```data_set```

---
## 📁 Project Structure
```txt
.
├── models/           
├── notebooks/          # Jupyter notebooks for training
├── dataset/            
│   ├── train/
│   └── test/
├── app.py              
└── requirements.txt    # Installation dependencies
```
## ⚠️ Disclaimer

*This tool is intended for educational and research purposes only. It is not a certified medical device. All predictions should be verified by a professional radiologist.*

---
