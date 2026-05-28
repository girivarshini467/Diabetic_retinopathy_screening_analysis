# Diabetic Retinopathy Detection using Deep Learning

## Project Overview

This project builds a Deep Learning-based medical image classification system to detect Diabetic Retinopathy (DR) from retinal fundus images using Transfer Learning with EfficientNetB0.

The system classifies retinal images into 5 stages of diabetic retinopathy severity and also generates Grad-CAM visualizations to highlight disease-affected regions in the retina.

This project demonstrates:
- Medical image preprocessing
- Deep learning classification
- Transfer learning
- Explainable AI (Grad-CAM)
- Model evaluation techniques

---

# Problem Statement

Diabetic Retinopathy is a diabetes complication that affects the eyes and can lead to blindness if not detected early.

Manual screening by ophthalmologists is time-consuming and expensive.

This project automates DR screening using Convolutional Neural Networks (CNNs).

---

# Dataset

Dataset Used:

APTOS 2019 Blindness Detection Dataset

Dataset Source:
- Kaggle APTOS 2019
- Downloaded using KaggleHub

Dataset Classes:

| Label | Class Name |
|------|------|
| 0 | No DR |
| 1 | Mild |
| 2 | Moderate |
| 3 | Severe |
| 4 | Proliferative DR |

---

# Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

# Deep Learning Architecture

Model Used:
- EfficientNetB0 (Transfer Learning)

Additional Layers:
- GlobalAveragePooling2D
- Dense Layer
- Dropout Layer
- Softmax Output Layer

---

# Project Workflow

1. Download Dataset
2. Load CSV Labels
3. Image Preprocessing
4. Data Augmentation
5. Transfer Learning using EfficientNetB0
6. Model Training
7. Model Evaluation
8. Confusion Matrix Generation
9. Classification Report
10. Grad-CAM Visualization
11. Single Image Prediction

---

# Image Preprocessing Techniques

The following preprocessing methods were applied:

- Image Resizing
- CLAHE Contrast Enhancement
- RGB to LAB Color Conversion
- Image Normalization

Purpose:
- Improve retinal vessel visibility
- Enhance lesion detection
- Improve model accuracy

---

# Data Augmentation

Data augmentation was used to improve model generalization.

Techniques Used:
- Rotation
- Zoom
- Width Shift
- Height Shift
- Horizontal Flip
- Shear Transformation

---

# Handling Class Imbalance

The dataset is highly imbalanced.

To address this issue:
- Class Weights were computed using Scikit-learn
- Weighted loss training was applied

This helps the model learn minority classes better.

---

# Training Configuration

| Parameter | Value |
|------|------|
| Image Size | 224x224 |
| Batch Size | 8 |
| Epochs | 10 |
| Optimizer | Adam |
| Learning Rate | 0.001 |
| Loss Function | Categorical Crossentropy |

---

# Model Evaluation Metrics

The following metrics were used:

- Accuracy
- Loss
- Classification Report
- Confusion Matrix
- Quadratic Weighted Kappa (QWK)

QWK is important for medical image classification tasks.

---

# Grad-CAM Visualization

Grad-CAM was implemented to make the model explainable.

It highlights retinal regions responsible for predictions.

Benefits:
- Improves interpretability
- Helps understand model decisions
- Makes the AI system more trustworthy

---

# Sample Output

The system produces:

- Predicted DR Stage
- Confidence Score
- Accuracy Graph
- Loss Graph
- Confusion Matrix
- Grad-CAM Heatmap

Example Prediction:

Predicted Class:
Moderate DR

Confidence:
94.52%
