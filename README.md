# Comparative Study of Emerging DL Models in Brain Tumor Detection (BTD) 🧠

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Framework-PyTorch%2FTensorFlow-orange.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

> [cite_start]Official repository for the paper **"Comparative Study of Emerging DL Models in BTD"**[cite: 1, 2]. 

## 📌 Overview
[cite_start]Detecting brain tumors from MRI scans is a critical step in clinical management and treatment planning[cite: 5]. [cite_start]Manual interpretation is time-consuming and prone to subjective differences[cite: 6, 14, 15]. 

[cite_start]This project benchmarks state-of-the-art Deep Learning (DL) architectures to classify brain MRI scans into tumor and non-tumor categories[cite: 7]. [cite_start]We compare traditional Convolutional Neural Networks (CNNs) against modern, transformer-inspired architectures to evaluate their efficiency, robustness, and ability to capture both local textures and global spatial contexts[cite: 7, 9].

## 🏗️ Models Evaluated
[cite_start]The following architectures were modified with a custom classifier (dropout rate of 0.5) and trained for binary classification[cite: 68]:
* [cite_start]**VGG19:** Traditional lightweight 3x3 convolutional filters[cite: 76].
* [cite_start]**ResNet50:** Residual learning framework for highly generalized feature extraction[cite: 76].
* [cite_start]**DenseNet121:** Dense connectivity network, highly effective for extracting small discriminative features in medical imaging[cite: 76].
* [cite_start]**ConvNeXt-Tiny:** A modern CNN incorporating Vision Transformer (ViT) design elements to model long-range dependencies[cite: 24, 76].
* [cite_start]**EfficientNet-B0:** Scaled architecture fine-tuned for stable convergence and strong generalization[cite: 76].

## 📊 Dataset
[cite_start]The dataset aggregates diverse, open-source MRI scans from Kaggle, Figshare, Ultralytics, SciDB, Roboflow, and Mendeley Data[cite: 49]. 

* [cite_start]**Total Images:** 13,692 MRI scans [cite: 53]
* [cite_start]**Classes:** Perfectly balanced between 6,846 Tumor (`Yes`) and 6,846 Non-Tumor (`No`) images[cite: 53].
* [cite_start]**Preprocessing:** Images were resized to 224x224 pixels[cite: 56]. [cite_start]Data augmentation included randomized horizontal/vertical flips, rotations, color jitter, grayscale conversion, and perspective transformations to ensure robust generalization[cite: 56]. [cite_start]No external static intensity normalization was applied to preserve real-world clinical variances[cite: 57].

## 🚀 Results
[cite_start]The models were trained using the Adam optimizer (learning rate: 0.0001, weight decay: 0.001) with Cross-Entropy loss[cite: 70, 71]. [cite_start]Below are the performance metrics evaluated on the test set after **15 Epochs**[cite: 86].

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **EfficientNet** | **92.24%** | **92.42%** | 91.97% | **92.19%** |
| **ConvNeXt-Tiny** | 92.11% | 92.36% | 91.82% | 92.09% |
| **ResNet50** | 92.06% | 91.86% | **92.31%** | 92.08% |
| **DenseNet121** | 91.97% | 91.93% | 92.02% | 91.97% |
| **VGG19** | 91.97% | 92.50% | 91.33% | 91.92% |

### Key Findings
* [cite_start]**Modern Architectures Dominate:** EfficientNet and ConvNeXt-Tiny outperformed traditional CNNs, demonstrating superior feature-extraction capabilities and convergence stability[cite: 88, 122, 123].
* [cite_start]**Generalization:** The optimized architectures surpassed the 92% accuracy mark, proving highly resilient to the structural anomalies and fluctuating intensities inherent in heterogeneous MRI data[cite: 76, 128].

## 👥 Authors
This research was conducted at the **School of Computer Engineering, KIIT DU, Bhubaneswar, India**.
* Adnan Hasan
* Ishaan Mishra
* Jyotiska Bose
* Jada Viswa Chaitanya Sai
* Jai Kumar
* Kaif Akhter
* Ranjita Kumari Dash

## 📬 Contact
For questions regarding the codebase or the paper, please reach out via email:
`ishaanmishral11@gmail.com`
