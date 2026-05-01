# 🏏 JU-Cricket: Cricket Action Classification using Deep Learning

## 📌 Overview
**JU-Cricket** is a deep learning-based project focused on automatic classification of cricket actions from images. The system leverages state-of-the-art Convolutional Neural Networks (CNNs) to identify and classify different cricket activities such as **Batting, Bowling, Fielding, and Umpire actions**.

This project is developed as part of academic research to contribute toward **sports analytics, intelligent video understanding, and automated decision systems**.

---

## 🎯 Objectives
- Build a robust **multi-class classification model** for cricket actions  
- Compare multiple deep learning architectures  
- Analyze model behavior using **Grad-CAM visualization**  
- Evaluate performance under **real-world distortions**

---

## 📂 Dataset Structure

### 🏷️ Classes
- Batting  
- Bowling  
- Fielding  
- Umpire Actions  

### 📌 Dataset Features
- Real-world cricket images  
- Multiple distortion types (blur, noise, compression)  
- Variations in lighting, pose, and background  

---

## 🧠 Models Used
The following pre-trained CNN architectures were fine-tuned:

- ResNet50  
- DenseNet121  
- EfficientNetB0  
- MobileNetV2  
- InceptionNet  
- XceptionNet  

### 🔧 Model Configuration
- Transfer Learning with ImageNet weights  
- Custom classifier head:
  - BatchNormalization  
  - Dense Layer (ReLU)  
  - Dropout  
  - Output Layer (Softmax)  

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Image resizing and normalization  
- Data augmentation (flip, rotation, zoom)

### 2. Training
- Optimizer: Adam  
- Loss Function: Categorical Crossentropy  
- Fine-tuning deeper layers  

### 3. Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix  

### 4. Explainability
- Grad-CAM used to visualize important regions in images  

---

## 📊 Results
- High classification accuracy achieved across all models  
- DenseNet and ResNet performed best overall  
- Models remained robust under distorted conditions (Task B)  
- Grad-CAM confirms focus on relevant regions (bat, ball, player posture)

---

## 🚀 How to Run

### 1. Clone Repository
```bash
git clone https://github.com/your-username/ju-cricket.git
cd ju-cricket
