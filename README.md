# 🌟 Image Generation with DCGAN in PyTorch

## 📌 Overview
This repository implements **Deep Convolutional GAN (DCGAN)** in **PyTorch** for generating high-quality images from random noise. It builds upon the concepts of **Vanilla GAN** and improves performance using convolutional architectures.

---

## 📖 Table of Contents
- [Introduction to GANs](#introduction-to-gans)
- [Vanilla GAN vs. DCGAN](#vanilla-gan-vs-dcgan)
- [DCGAN Architecture](#dcgan-architecture)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [References](#references)

---

## 🔥 Introduction to GANs
**Generative Adversarial Networks (GANs)** are a class of deep learning models used for **generating realistic data**. A GAN consists of:
1. **Generator (G)**: Generates fake images from random noise.
2. **Discriminator (D)**: Tries to distinguish real images from fake ones.

Both networks compete in a game-like setting, improving each other over time.

---

## ⚡ Vanilla GAN vs. DCGAN

### ✅ Vanilla GAN
- Uses fully connected layers (MLPs).
- Struggles with **image quality and stability**.
- Harder to train due to vanishing gradients.

### ✅ DCGAN (Deep Convolutional GAN)
- Uses **Convolutional and Transposed Convolutional layers**.
- Generates **higher quality** images.
- Stabilized training using **Batch Normalization & LeakyReLU**.
- Works better on **large-scale image datasets**.

---

## 🎯 DCGAN Architecture
### **1️⃣ Generator (G)**
- Converts **random noise (latent vector) into realistic images**.
- Uses **ConvTranspose2d** layers for **upsampling**.
- Activation: **ReLU** & **Tanh**.

### **2️⃣ Discriminator (D)**
- Classifies **real vs. fake images**.
- Uses **Conv2d** layers for **downsampling**.
- Activation: **LeakyReLU & Sigmoid**.

---

## 📁 Project Structure
```bash
📂 Image_Generation_with_DCGAN
├── 📂 data                  # Dataset storage
├── 📂 images                # Generated images during training
├── 📜 dcgan.py              # DCGAN model (Generator + Discriminator)
├── 📜 train.py              # Training loop
├── 📜 utils.py              # Utility functions
├── 📜 requirements.txt      # Required dependencies
└── 📜 README.md             # Project documentation (this file)
```

---

## 🛠 Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/nikhilScripts/Generative-Adversarial-Networks.git
pip install -r requirements.txt
```

---

## 🚀 Usage
### **1️⃣ Train DCGAN**
```bash
python train.py
```
### **2️⃣ Generate Images**
After training, generate new images using:
```python
python generate.py
```

---

## 🎨 Results
Here are sample images generated after training DCGAN for **20 epochs**:
![Generated Images](images/sample.png)

---

## 📚 References
1. **Original DCGAN Paper**: [Radford et al. (2015)](https://arxiv.org/abs/1511.06434)
2. **PyTorch GAN Tutorial**: [Official PyTorch Guide](https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html)

---

## 🤝 Contributing
Feel free to contribute to improve this project. Fork the repo, make changes, and create a pull request! 🚀

