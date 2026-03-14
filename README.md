# Computer-Vision-Research-Implementation

## 📚 References & Official Papers



![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-red)
![Status](https://img.shields.io/badge/Status-Active_Development-brightgreen)

## 📌 Overview
This repository contains ground-up, modular implementations of foundational and state-of-the-art Computer Vision architectures in **PyTorch**. The goal of this project is to deeply understand the mathematical and architectural nuances of these models by building them from scratch, avoiding high-level wrapper libraries.

By implementing these papers, this repository covers the three core pillars of Computer Vision:
1. **Image Classification** (Feature Extraction & Depth)
2. **Semantic Segmentation** (Spatial Localization & Encoder-Decoder structures)
3. **Object Detection** (Real-time inference & Advanced optimizations)

---

## 📄 Papers Implemented

### 1. VGG-19 (Classification)
* **Paper:** *Very Deep Convolutional Networks for Large-Scale Image Recognition* [cite: 953]
* **Key Learnings:** Understanding how a deep stack of small $3\times3$ convolutional filters can effectively replace larger receptive fields [cite: 956, 1008], improving decision function discrimination while reducing parameters[cite: 1021].
* **VGG-19:** [Very Deep Convolutional Networks for Large-Scale Image Recognition](https://arxiv.org/abs/1409.1556) (Simonyan & Zisserman, 2014) [cite: 190, 951]
* **Status:** `In Progress`

### 2. U-Net (Segmentation)
* **Paper:** *U-Net: Convolutional Networks for Biomedical Image Segmentation* [cite: 2]
* **Key Learnings:** Implementing a symmetric u-shaped architecture with a contracting path to capture context and an expanding path for precise localization[cite: 11, 63]. Grasping the concept of skip connections to retain spatial information.
* **U-Net:** [Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/abs/1505.04597) (Ronneberger et al., 2015) [cite: 1]
* **Status:** `Planned`

### 3. YOLOv7 (Object Detection)
* **Paper:** *YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors* [cite: 197, 198]
* **Key Learnings:** Advanced architecture design including Extended-ELAN (E-ELAN) [cite: 326], planned re-parameterized convolutions [cite: 388, 418], and dynamic label assignment strategies (coarse-to-fine lead guided assigner)[cite: 248].
* **YOLOv7:** [Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors](https://arxiv.org/abs/2207.02696) (Wang et al., 2022) [cite: 196]
* **Status:** `Planned`

---

## 📂 Repository Structure

The codebase is structured for scalability and production-readiness:

```text
Computer-Vision-Research-Implementation/
│
├── models/                  # Core architectural definitions (PyTorch nn.Module)
│   ├── vgg.py               # VGG-19 implementation
│   ├── unet.py              # U-Net implementation
│   └── yolov7/              # YOLOv7 modules (E-ELAN, RepConv, etc.)
│
├── utils/                   # Helper functions
│   ├── dataset.py           # Custom PyTorch Dataset classes and Dataloaders
│   └── metrics.py           # Evaluation metrics (IoU, mAP, etc.)
│
├── train.py                 # Modular training loop with validation
├── test.py                  # Inference and evaluation script
│
├── demo.ipynb               # Jupyter Notebook for visualization and easy testing
└── requirements.txt         # Environment dependencies
