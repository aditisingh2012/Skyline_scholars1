# 🌄 Off-Road Semantic Segmentation using DINOv2  
## Team: Skyline_Scholars

### 👩‍💻 Team Members
- Aditi Singh  
- Jivisha Dharmadhikari  
- Khushi Gautam  
- Dixita Nema  

---

## 📌 Project Overview

This project implements **semantic segmentation for off-road terrain images** using a pretrained **DINOv2 Vision Transformer backbone** combined with a custom segmentation head.

The goal is to classify each pixel in off-road driving scenes into meaningful categories (terrain, obstacles, vegetation, sky, etc.) to assist in autonomous navigation systems.

We leverage pretrained transformer-based representations to improve segmentation performance with limited training epochs.

---

## 🧠 Model Architecture

### 🔹 Backbone
- DINOv2 Vision Transformer (ViT-S/14)
- Patch-based feature extraction
- Pretrained weights for strong representation learning

### 🔹 Segmentation Head
- Linear classifier over patch embeddings
- Patch tokens reshaped into spatial grid
- Upsampling to match image resolution

### 🔹 Input Configuration
- Images resized to match backbone requirements
- Patch size: 14×14
- Normalization using ImageNet statistics

---

## 📂 Dataset

Dataset used:
- Offroad_Segmentation_training dataset
- Offroad_Segmentation_testimages

Data split:
- Training set
- Validation set

For faster experimentation:
- 900 training samples
- 500 validation samples

---

## ⚙️ Training Configuration

| Parameter | Value |
|------------|--------|
| Epochs | 10 |
| Batch Size | 10 |
| Optimizer | Adam |
| Learning Rate | 1e-4 |
| Loss Function | CrossEntropyLoss |
| Device | CPU |

---

## 📊 Final Results (After 3 Epochs)

| Metric | Value |
|--------|--------|
| Final Validation Loss | 0.8154 |
| Final IoU | 0.2934 |
| Final Dice Score | 0.4382 |
| Final Pixel Accuracy | 0.7026 |

---

## 📈 Training Outputs

Generated files:

- training_curves.png  
- iou_curves.png  
- dice_curves.png  
- all_metrics_curves.png  
- evaluation_metrics.txt  

