# Transfer Learning for Insect Image Classification

This project explores the use of transfer learning for image classification using a pretrained ResNet-18 model. The goal is to classify three insect classes (cockroach, scorpion, and spider) and compare different fine-tuning strategies under varying dataset sizes.

---

## 📌 Project Objectives

- Apply transfer learning using a pretrained convolutional neural network.
- Replace the model head to adapt the network to a new classification task.
- Compare two transfer learning strategies:
  - Full fine-tuning (training all layers)
  - Head-only training (freezing the backbone and training only the classifier)
- Evaluate both strategies on:
  - A small dataset (20% of training data)
  - A large dataset (full training data)
- Compare performance and training time across all settings.

---

## 🗂 Dataset

- Source: Kaggle — *Spiders, Scorpion, and Cockroach Dataset*
- Number of classes: 3
  - Cockroach
  - Scorpion
  - Spider
- Images are resized to 224×224 pixels.
- Dataset is split into training, validation, and test sets.
- Two training sizes are used:
  - Small dataset: 20% of training samples
  - Large dataset: 100% of training samples

---

## 🧠 Model

- Architecture: ResNet-18 pretrained on ImageNet.
- The original classification head is replaced with a new fully connected layer with 3 output units.
- Loss function: Cross-entropy loss
- Optimizer: Adam
- Batch size: 32
- Early stopping is applied during training to prevent overfitting.

---


---
