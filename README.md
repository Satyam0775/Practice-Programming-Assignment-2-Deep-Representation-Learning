# 🧠 Practice Programming Assignment 2 — Advanced Deep Representation Learning
**Author:** Satyam Kumar  
**Instructor:** Prof. Prathosh A. P.  
**Date:** August 17, 2025  

---

## 📘 Overview
This repository contains the complete implementation, training outputs, and final results for **Practice Programming Assignment 2**, part of the *Advanced Deep Representation Learning* course under **Prof. Prathosh A. P.** (IISc, Bangalore).

The assignment explores:
- Variational Autoencoders (VAE)
- Vector Quantized VAE (VQ-VAE)
- CNN-based classification
- Latent-space classification (MLP)
- Gaussian Mixture Model (GMM) sampling

All experiments were executed in Google Colab using PyTorch.

---

## 📦 Full Project Files
📂 **All Code, Models & Results (Colab)**  
👉 Google Drive: https://drive.google.com/drive/folders/1jFx33bm2s1dUYCrw-bp2Td291NZ2uIcy?usp=sharing

📂 **Datasets Used**
- **Animals Dataset** (5316 images, 90 classes) → Task 1 + FID reference  
- **Butterfly Dataset** (60 images, 1 class) → Tasks 2–5  

---

## 🧩 Tasks Implemented

| Task | Description | Key Result |
|------|-------------|------------|
| **1** | Vanilla VAE, z-sampling {1,5,10}, reconstruction grids, loss curves, FID | **FID: 249.12** |
| **2** | CNN classifier (Butterfly dataset) | **100% Accuracy** |
| **3** | VAE latent extraction → MLP classifier | **100% Accuracy** |
| **4** | VQ-VAE, discrete latent extraction → MLP classifier | **100% Accuracy** |
| **5** | GMM fitted on VAE latents → sampling → decoder → 10×10 grid | Completed |

---

## 📊 Key Results

### Task 3 — VAE Latent Space Classification
Latent shape: torch.Size([60, 128])
Labels: torch.Size([60])

Training MLP on VAE latents...
Epoch 5 Loss = 0.0000
Epoch 10 Loss = 0.0000
Epoch 15 Loss = 0.0000
Epoch 20 Loss = 0.0000

MLP Accuracy: 100%


### Task 4 — VQ-VAE Training Log


Epoch 1/8 Loss = 0.6843
Epoch 2/8 Loss = 0.7257
Epoch 3/8 Loss = 0.6455
Epoch 4/8 Loss = 0.5920
Epoch 5/8 Loss = 0.5504
Epoch 6/8 Loss = 0.5583
Epoch 7/8 Loss = 0.6023
Epoch 8/8 Loss = 0.6055

VQ-VAE Training Done!
MLP Accuracy on VQ Latents: 100%


### Task 1 — VAE FID Score


FID Score (1000 generated images): 249.12


---

## 🎨 Visual Results
Available in the attached Drive or results folder:
- VAE Reconstruction Grids (10×10)
- VAE Generation Grids (10×10)
- Loss Curves (Reconstruction, KL, Total)
- VQ-VAE Reconstructions
- GMM-based Sample Grid (10×10)

---

## ⚙️ Environment
- Google Colab (Free GPU)
- Python 3.10+
- PyTorch 2.x
- Torchvision
- Scikit-Learn
- CleanFID
- SciPy
- Matplotlib

---

## 🚀 How to Run
1. Open the `.ipynb` notebook in **Google Colab**
2. Mount Google Drive and set dataset paths:
   ```python
   animals_path   = "/content/drive/MyDrive/Task 2/animals"
   butterfly_path = "/content/drive/MyDrive/Task 2/butterfly"


Run all cells sequentially

Visual outputs and models will save automatically

🧑‍🎓 Author’s Note

This assignment demonstrates the full pipeline of representation learning:

VAEs for continuous latent modeling

VQ-VAE for discrete latent encoding

CNN vs. MLP classification

Latent-space analysis

Probabilistic sampling using GMMs

While generated images appear smooth or blurry (typical for VAEs trained briefly on high-resolution data), every task requirement is successfully completed with correct methodology and results.
