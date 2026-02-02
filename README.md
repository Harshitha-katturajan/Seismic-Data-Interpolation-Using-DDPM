# Seismic Data Interpolation using DDPM

![Seismic Interpolation Result](images/Interpolation%201.png)
*Figure 1: Performance comparison showing Ground Truth, Masked Input (dead traces), and 100-epoch DDPM Reconstruction.*

This repository implements a **Denoising Diffusion Probabilistic Model (DDPM)** specifically for seismic trace interpolation. The model learns to reconstruct missing geophysical data to ensure structural continuity in subsurface imaging.

---

## 🛠 Work Performed
* **Data Pipeline**: Developed a custom dataset handler for 224x224 seismic patches.
* **Normalization**: Applied robust $3\sigma$ (standard deviation) scaling to preserve amplitude polarity and geophysical signal integrity.
* **Masking**: Integrated a vertical trace masking system to simulate missing acquisition gaps (dead traces).
* **Architecture**: Designed a 1-channel U-Net featuring sinusoidal time-embeddings, specifically optimized for grayscale seismic data.
* **Inference**: Implemented a constrained inpainting algorithm to ensure generated traces are geophysically consistent with surrounding known data.

## 📈 Training Performance
* **Loss Function**: Utilized Mean Squared Error (MSE) to minimize the distance between predicted and actual noise.
* **Final Loss**: Achieved a final training loss of **0.00318** after 100 epochs on the seismic dataset.



## 🚀 Technical Stack
* **Framework**: PyTorch
* **Visualization**: Matplotlib using the industry-standard `RdBu` (Red-Blue) colormap
* **Environment**: Kaggle GPU (P100/T4)

## 📁 Repository Structure
* `ddpm-sesmic.ipynb`: Core notebook containing architecture, training logs, and inference logic.
* `images/`: Directory containing qualitative result plots.

---
## 🏛 Institutional Credit
This work was developed during my **Research Internship at C-DAC (Centre for Development of Advanced Computing)**, Chennai. The project explores the application of Deep Diffusion Models for advanced geophysical data processing.

**Harshitha K.**
*Final Year B.E. Computer Science and Engineering Student*
*AIML Lead, GDG JEC Chapter*
