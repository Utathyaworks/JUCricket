# 🏏 JU-Cricket: A Benchmark Dataset for Robust Cricket Action Classification

## 📌 Overview
JU-Cricket is a large-scale benchmark dataset and experimental framework designed for **fine-grained cricket action classification under realistic visual conditions**. Unlike existing datasets, JU-Cricket focuses on **real-world deployment challenges**, including visual distortions commonly present in broadcast footage such as motion blur, noise, and low resolution.

This project bridges the gap between **academic performance and real-world applicability** in sports analytics and computer vision.

---

## ❗ Problem Statement
Cricket action recognition is inherently challenging due to:

- High **visual similarity between actions** (e.g., pull vs cut shot)  
- **Single-frame critical decision points** (bat-ball contact, umpire signals)  
- Severe **visual distortions in broadcast footage**:
  - Motion blur  
  - Lens flare  
  - Low resolution  
  - Compression artifacts  

Existing datasets fail because they are:
- Small and limited in scope  
- Focused on single roles (only batting or bowling)  
- Captured under clean, unrealistic conditions  

---

## 🚀 Key Contributions

### 🥇 JU-Cricket Dataset
- **15,728 images** derived from **1,966 original images**
- Each image includes **7 distortion variants + original**
- Designed to simulate **real broadcast conditions**

### 🧩 Multi-Role Coverage
- Batting  
- Bowling  
- Fielding  
- Umpiring  

### 🧠 Fine-Grained Understanding
- **20+ sub-actions**, including:
  - Batting: Cut, Drive, Sweep, Scoop, Pull, etc.  
  - Bowling: Fast, Spin  
  - Fielding: Catch, Run-out, Stumping, etc.  
  - Umpiring: Six, Out, No-ball, Wide, etc.  

### 🧱 Hierarchical Problem Formulation
- **Task A (Coarse Classification)**  
  → Identify player role (4 classes)

- **Task B (Fine-Grained Classification)**  
  → Identify specific sub-action (20+ classes)

---

## ⚠️ Why This Problem is Hard
- Key discriminative features are:
  - **Bat angle**
  - **Wrist movement**
  - **Body posture**
- These features are highly sensitive to:
  - Blur  
  - Noise  
  - Resolution loss  

👉 Even small distortions can break classification performance.

---

## 🧠 Models Benchmarked

### 🔹 CNN-Based Models
- ResNet50  
- DenseNet121  
- EfficientNetB0  
- MobileNetV2  
- InceptionNet  
- XceptionNet  

### 🔹 Transformer-Based Models
- Vision Transformer (ViT)

### 🔹 Vision-Language Models
- CLIP (ViT-based)
  - Zero-shot  
  - Fine-tuned  
  - Text-supervised  

---

## 🧪 Experimental Setup
- Training on **NVIDIA Tesla P100 GPU**
- Batch size: 32  
- Optimizer: Adam  
- Learning rate: 1e-4  
- Loss: Categorical Crossentropy  

### Training Strategies
- From-scratch training  
- ImageNet pretrained fine-tuning  

---

## 📊 Key Findings

### 🔥 1. Pretraining Matters More Than Architecture
- Significant performance gain:
  - **+0.22 (Task A)**
  - **+0.18 (Task B)**  

👉 Transfer learning is critical for real-world robustness.

---

### 🔥 2. Fine-Grained Classification is Extremely Difficult
- Actions differ by subtle motion cues
- Distortions destroy key features

Examples:
- Cut vs Pull → both horizontal bat  
- Sweep vs Scoop → similar posture  

---

### 🔥 3. CLIP Limitations
- Performs reasonably on coarse classification  
- Fails on fine-grained actions  

👉 Insight:
> Language supervision does not transfer well to biomechanical action understanding without domain adaptation.

---

## 📉 Dataset Realism Advantage
Unlike traditional datasets:
- JU-Cricket includes **distorted images in training AND testing**
- Ensures evaluation reflects **real deployment conditions**

👉 Measures **robustness, not just accuracy**

---

## 📂 Dataset Highlights

- Total Images: **15,728**
- Train / Val / Test:
  - 9,928 / 2,576 / 3,224  
- 8 variants per image:
  - Original + 7 distortions  

### Distortion Types
- Motion Blur  
- Gaussian Noise  
- Low Resolution  
- Lens Flare  
- Chromatic Aberration  
- Dirty Lens  

---

## 🔍 Applications
- Sports analytics  
- Automated highlight generation  
- Coaching and performance analysis  
- Umpire decision assistance  
- Broadcast intelligence systems  

---

## 📈 Future Work
- Extend to **video-based action recognition**  
- Improve **CLIP with domain-specific prompts**  
- Explore **Vision Transformers + Temporal Models**  
- Real-time deployment systems  

---

## 🧠 One-Line Summary
JU-Cricket is the first benchmark dataset that combines **multi-role classification, fine-grained hierarchical labeling, and realistic visual distortions**, enabling robust evaluation of modern deep learning models under real-world cricket scenarios.

---

## 👨‍💻 Authors
- Utathya Aich  
- Aritra Mondal  
- Pawan Kumar Singh  

---

## 🔗 Repository
https://github.com/aritra-mondal-it/JUCricket

---

## 📜 License
For academic and research purposes only.
