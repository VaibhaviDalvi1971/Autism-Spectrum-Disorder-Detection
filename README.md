# 🧠 SpecTruFace: Autism Spectrum Disorder Detection (ML-Based)

🚀 **Machine Learning system for Autism Spectrum Disorder (ASD) detection using facial landmark analysis**

---

## 📌 Overview

**SpecTruFace** is a Machine Learning-based system designed to identify potential indicators of **Autism Spectrum Disorder (ASD)** from facial images.

The system analyzes facial structure using landmark-based feature extraction and classifies images into **Autistic** or **Non-Autistic** categories.

💡 This project is implemented entirely using **Google Colab**, focusing on the core Machine Learning pipeline.

---

## 🎯 Objective

* Detect ASD using facial landmark analysis
* Build a lightweight classification model
* Extract meaningful geometric facial features
* Develop an efficient and interpretable ML pipeline

---

## 🧠 Methodology

### 🔄 Processing Pipeline

1. 📥 Input facial image
2. 🧍 Face detection using MTCNN / Dlib
3. 📍 Extract 68 facial landmarks
4. 📏 Compute geometric facial features
5. 🤖 Train Machine Learning model (Random Forest)
6. 📊 Generate prediction (ASD / Non-ASD)

---

## 🔍 Feature Engineering

Facial landmarks are transformed into a **9-dimensional feature vector**:

### 📐 Distance-Based Features

* Left eye width
* Right eye width
* Mouth width
* Nose to mouth distance (left & right)
* Jaw width

### 📊 Ratio-Based Features

* Eye Aspect Ratio (left & right)
* Facial symmetry ratio

👉 Features are computed using **Euclidean distance between landmark points**

---

## 🤖 Model Details

| Parameter       | Description                           |
| --------------- | ------------------------------------- |
| Model           | Random Forest Classifier              |
| Feature Type    | Geometric facial features             |
| Input Dimension | 9                                     |
| Output          | Binary Classification (ASD / Non-ASD) |

---

## 📂 Project Structure

```bash
📁 project/
│── autism_predictor.py        # ML pipeline & prediction logic
│── autism_rf_classifier.pkl   # Trained model
│── dataset/
│    ├── train/
│    └── test/
```

---

## ⚙️ Environment & Setup

This project is designed to run on **Google Colab**.

### 🔹 Steps

1. Open Google Colab
2. Upload the project file
3. Mount Google Drive
4. Install dependencies

```bash
!pip install mtcnn opencv-python dlib imutils scikit-learn xgboost matplotlib tqdm lz4
```

---

## ▶️ Usage

### 🔹 Training

* Extract features from dataset
* Train Random Forest model
* Save trained model

```bash
python autism_predictor.py
```

---

### 🔹 Prediction

* Input an image
* Detect face and extract landmarks
* Compute features
* Generate classification output

---

## ⚠️ Limitations

* Relies on handcrafted features
* Performance depends on image quality
* Limited ability to capture complex patterns
* Dataset size and diversity may affect results

---

## 🚀 Future Improvements

* Integrate Deep Learning models (CNN-based)
* Increase dataset size and diversity
* Enhance feature extraction techniques
* Apply Explainable AI methods
* Improve overall model performance

---

## 🌟 Summary

This project demonstrates the application of **Machine Learning and Computer Vision** techniques for ASD detection using **facial landmark-based feature extraction**, highlighting both the potential and limitations of feature-based approaches.

---
