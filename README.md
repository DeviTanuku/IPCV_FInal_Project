# 🖼️ Image Deblurring Using Deep Learning: SRCNN vs. ViT-DeblurNN

> 🎓 **Course:** Image Processing and Computer Vision  
> 👥 **Team Members:** Antra, Devi, Kartik, Chandana, Jaspreet  
> 📂 **Models:** SRCNN (CNN-based) & ViT-DeblurNN (Transformer-based)  
> 📁 **Dataset:** GoPro Motion Deblurring Dataset

---

## 📝 Project Description

This project presents a comparative study of two deep learning models — **SRCNN** and **ViT-DeblurNN** — for restoring blurred images. SRCNN offers fast and lightweight CNN-based restoration, while ViT-DeblurNN uses Vision Transformers to achieve superior deblurring quality. Evaluation is based on PSNR, SSIM, and visual comparison.

---

## 🎯 Objectives

- Implement two deep learning models for image deblurring.
- Use GoPro dataset with paired blurred and sharp images.
- Compare models using both quantitative and qualitative metrics.

---

## 🧪 Dataset

- **Name:** GoPro Deblurring Dataset  
- **Images:** 500 blurred images with ground truth sharp counterparts  
- **Preprocessing:**
  - Resized to 256×256 (SRCNN) and 224×224 (ViT)
  - Normalized pixel values
  - 70/15/15 train/val/test split

---

## 🧱 Model Overview

### SRCNN (CNN-Based)
- 3-layer convolutional network (9×9, 5×5, 5×5)
- Fast training (~5 mins)
- ~57K parameters

### ViT-DeblurNN (Transformer-Based)
- 6-layer encoder
- Handles global dependencies with 16×16 patches
- ~85M parameters, slower (~20 mins), but better quality

---

## 📊 Evaluation Metrics

| Model         | PSNR (↑) | SSIM (↑) | Parameters | Training Time |
|---------------|----------|----------|------------|----------------|
| SRCNN         | 28.5 dB  | 0.89     | 57K        | ~5 mins        |
| ViT-DeblurNN  | 30.2 dB  | 0.92     | 85M        | ~20 mins       |

---

## 📂 Repository Structure

Image_Deblurring_Project/ ├── IPCV_final.ipynb # Main notebook: training, results, comparison ├── IPCV_Presentation.pdf # Final presentation slides └── README.md # This file
