# JU-Cricket: A Benchmark Dataset for Fine-grained Cricket Action Classification with Challenging Visual Conditions

## 📌 Overview
JU-Cricket is a large-scale benchmark dataset and experimental framework designed for **fine-grained cricket action classification under realistic visual conditions**. Unlike existing datasets, JU-Cricket focuses on **real-world deployment challenges**, including visual distortions commonly present in broadcast footage such as motion blur, noise, and low resolution.

---

## ❗ Problem Statement
Cricket action recognition is challenging due to:
- High **visual similarity between actions**
- **Single-frame decision moments**
- Real-world **visual distortions**

---

## 🚀 Key Contributions
- **15,728 images** with distortion variants  
- Covers **4 roles + 20+ sub-actions**  
- Introduces **hierarchical classification (Task A & B)**  
- Benchmark across **CNNs, ViT, and CLIP**

---

## 🧩 Dataset Classes (with Examples)

### 🏏 Batting Actions

| Cut | Drive | Pull | Sweep |
|-----|------|------|-------|
| <img src="JU-Cricket_pictures/Batting/6_cut_main.jpg" width="160"/> | <img src="JU-Cricket_pictures/Batting/Batting_Drive_ju_cr_Drive_28.jpg" width="160"/> | <img src="JU-Cricket_pictures/Batting/Batting_PullShot_ju_cr_PullShot_39.png" width="160"/> | <img src="JU-Cricket_pictures/Batting/Batting_Sweep_ju_cr_Sweep_38.jpeg" width="160"/> |

| Scoop | Straight Drive | Leg Shot |
|------|----------------|-----------|
| <img src="JU-Cricket_pictures/Batting/Batting_Scoop_ju_cr_Scoop_12.jpeg" width="160"/> | <img src="JU-Cricket_pictures/Batting/Batting_Straight_ju_cr_Straight_39.jpg" width="160"/> | <img src="JU-Cricket_pictures/Batting/Batting_Leg_Shot_ju_cr_Leg_Shot_78.png" width="160"/> |

---

### 🎯 Bowling Actions

| Fast Bowling | Spin Bowling |
|-------------|-------------|
| <img src="JU-Cricket_pictures/Bowling/Bowling_fast_bowl_ju_cr_fast_bowl_06.jpeg" width="200"/> | <img src="JU-Cricket_pictures/Bowling/Bowling_spin_bowl_ju_cr_spin_bowl_23.jpeg" width="200"/> |

---

### 🧤 Fielding Actions

| Catch | Run Out | Stumping |
|------|--------|----------|
| <img src="JU-Cricket_pictures/Fielding/Fielding_catching_a_ball_ju_cr_catching_a_ball_21.jpeg" width="160"/> | <img src="JU-Cricket_pictures/Fielding/Fielding_run_out_ju_cr_run_out_01.jpeg" width="160"/> | <img src="JU-Cricket_pictures/Fielding/Fielding_stumping_ju_cr_stumping_07.jpeg" width="160"/> |

| Diving Stop | Boundary Save |
|------------|--------------|
| <img src="JU-Cricket_pictures/Fielding/Fielding_diving_stop_ju_cr_diving_stop_08.jpg" width="200"/> | <img src="JU-Cricket_pictures/Fielding/Fielding_boundary_save_ju_cr_boundary_save_12.jpeg" width="200"/> |

---

### 👨‍⚖️ Umpire Actions

| Six | Four | Out |
|----|-----|-----|
| <img src="JU-Cricket_pictures/Umpire/Umpire_Six_ju_cr_Six_24.jpeg" width="160"/> | <img src="JU-Cricket_pictures/Umpire/Umpire_Four_ju_cr_Four_06.jpeg" width="160"/> | <img src="JU-Cricket_pictures/Umpire/Umpire_Out_ju_cr_Out_03.jpg" width="160"/> |

| Wide | No Ball | Leg Bye |
|------|--------|--------|
| <img src="JU-Cricket_pictures/Umpire/Umpire_Wide_ju_cr_Wide_01.jpeg" width="160"/> | <img src="JU-Cricket_pictures/Umpire/Umpire_No_ball_ju_cr_No_ball_13.jpg" width="160"/> | <img src="JU-Cricket_pictures/Umpire/Umpire_Leg_Bye_ju_cr_Leg_Bye_13.jpeg" width="160"/> |

---

## 🧠 Models Benchmarked

### 🔹 CNNs
ResNet50, DenseNet121, EfficientNetB0, MobileNetV2, InceptionNet, XceptionNet  

### 🔹 Transformers
Vision Transformer (ViT)  

### 🔹 Vision-Language Models
CLIP (Zero-shot, Fine-tuned, Text-supervised)

---

## 🧪 Experimental Setup
- GPU: NVIDIA Tesla P100  
- Optimizer: Adam  
- Learning Rate: 1e-4  
- Loss: Crossentropy  
- Training:
  - From scratch  
  - Pretrained fine-tuning  

---

## 📊 Key Findings

### 🔥 Pretraining > Architecture
- +0.22 improvement (Task A)  
- +0.18 improvement (Task B)  

### 🔥 Fine-Grained is Hard
- Small pose differences → large confusion  

### 🔥 CLIP Limitation
- Good at coarse tasks  
- Weak for fine-grained biomechanics  

---

## 📉 Dataset Realism
- Includes distortions in **train + test**
- Measures **robustness, not just accuracy**

---

## 📂 Dataset Stats
- Total: 15,728 images  
- Train / Val / Test: 9,928 / 2,576 / 3,224  
- 8 variants per image  

---

## 🔍 Applications
- Sports analytics  
- Highlight generation  
- Coaching tools  
- Broadcast AI  

---

## 📈 Future Work
- Video-based models  
- Temporal learning  
- Better CLIP adaptation  

---

## 👨‍💻 Authors
- Utathya Aich  
- Aritra Mondal  
- Pawan Kumar Singh  

---

## 🔗 Repository
https://github.com/Utathyaworks/JUCricket

---

## Dataset Availabilty
Dataset will be publicily available once the paper is accepted, but till then you can see some of the sample images as given in the table.

## 📜 License
Academic and research use only.
