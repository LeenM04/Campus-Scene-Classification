# TexMobile: A Texture-Aware Lightweight Framework for Campus Scene Classification 🏫

This repository contains the official implementation of **TexMobile**, a hierarchical deep learning framework designed to recognize complex campus environments.

## 🚀 Overview
TexMobile addresses challenges like architectural homogeneity and lighting variations by combining global scene context with fine-grained texture encoding. It leverages a dual-head architecture to distinguish between **Objects** and **Scenes** before performing final classification.

## 🧠 Key Features
* **Hierarchical Classification:** Jointly models coarse (Object vs. Scene) and fine-grained categories.
* **Texture Encoding:** Integrates a **Deep Texture Encoding Network (DeepTEN)** to capture subtle material patterns.
* **Lightweight Backbone:** Built on **MobileNetV2**, making it efficient for resource-constrained environments.
* **Custom Dataset:** Trained on a unique dataset of **2,405 images** collected from the **University of Jordan**.

## 📊 Performance Comparison
TexMobile outperforms standard baselines while remaining significantly more lightweight:

| Model | Parameters | Test Accuracy |
| :--- | :--- | :--- |
| MobileNetV2 (Vanilla) | ~2.2 M | 93.42% |
| DenseNet 121 | ~8.0 M | 94.18% |
| GoogleNet | ~6.6 M | 96.69% |
| **TexMobile (Ours)** | **~2.4 M** | **98.07%** |

## 📈 Results & Visualizations
The model achieves stable convergence with a final validation accuracy of approximately **97.5%**.
* **Fine-grained Accuracy:** 98.1%
* **Coarse-level Accuracy:** 98.4%

## 🛠️ Implementation Details
* **Framework:** PyTorch
* **Optimizer:** AdamW with a weight decay of $5\times10^{-4}$
* **Learning Rate:** Differential strategy ($1\times10^{-5}$ for backbone, $1\times10^{-4}$ for heads)
* **Input Resolution:** 224x224 pixels
* **Categories:** Person, Tree, Building, Car, and Lab

## 👥 Authors
* Jana Godieh
* Eithar Al-Salameh
* **Leen Almasarweh**
* Dana Abu Al-Ruz

**Instructor:** Tamam AlSarhan
**University:** University of Jordan
