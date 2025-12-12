# 🧠 Brain Tumor Classification & Severity Detection
A Hybrid Machine Learning Approach using MRI Scans

This project implements a hybrid interpretable machine learning pipeline for brain tumor classification and severity detection using MRI images.
Unlike deep learning “black-box” models, this system focuses on feature-engineered, explainable, and computationally efficient diagnosis — making it suitable for real clinical decision support.

The system performs two tasks:

Tumor Classification → Glioma, Meningioma, Pituitary, No Tumor
Severity Detection → Low, Mild, High, No Tumor

#Demo

<img width="976" height="580" alt="image" src="https://github.com/user-attachments/assets/41a8d4ef-bd91-4a85-8132-03194a6c5fd0" />

<img width="976" height="580" alt="image" src="https://github.com/user-attachments/assets/138a8c39-bc75-4187-b0b5-ce5d8976d7ea" />





# 📂 Dataset Description
👉 BRISC2025 MRI Dataset

Contains MRI images + segmentation masks.

Fine-grained classes (4-class):
0: Glioma
1: Meningioma
2: Pituitary
3: No Tumor

Coarse classes (2-class):
Tumor-present
Tumor-absent

Masks allow extraction of ROI-based geometric and intensity features.

# 📌 Key Features

Masks allow extraction of ROI-based geometric and intensity features.
🔹 Hybrid ML Pipeline (ROI + Global Features)

Uses a combination of:
Geometric features (Area, Perimeter, Solidity, Circularity)
Intensity statistics (Mean, Std, Min, Max)
Texture features (LBP, HOG, Gabor filters)
Gradient & edge-based features

🔹 Random Forest–based Dual-Classifiers

Two ML models trained using extracted features:
Model	Task	Accuracy
Random Forest	Tumor Type Classification	90.0%
Random Forest	Severity Classification	59.7%

🔹 Interactive Gradio Deployment

The user can upload MRI images and receive:
Tumor Presence
Tumor Type
Severity
Visual & color-coded explanation

# 🚀 How to Run the Project
1️⃣ Install Dependencies
pip install -r requirements.txt

2️⃣ Run the Gradio App
python app.py

3️⃣ Upload an MRI Image

You will receive:
Tumor detection
Classification
Severity level
Explanation

🧪 Tech Stack

Python
Scikit-learn (Random Forest)
OpenCV (Image Processing)
Albumentations (Mask Augmentation)
Skimage (HOG, LBP)
Gabor Filters
Numpy, Pandas
Gradio (Deployment UI)
