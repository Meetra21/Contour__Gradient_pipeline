# Contour & Gradient Feature Pipelines for Handwritten Character Recognition

This repository provides **baseline pipelines** for handwritten digit and letter recognition using **contour-based boundary features** and **central-difference image gradients**.  
Instead of convolutional networks, we train **MLP classifiers** directly on engineered gradient features.

---

## 📂 Repository Structure

- **Contour__Gradient_pipeline_for_Digits_Dataset.ipynb**  
  Pipeline for the [MNIST](http://yann.lecun.com/exdb/mnist/) digit dataset (0–9).
  
- **Contour__Gradient_pipeline_for_Letters_Dataset.ipynb**  
  Pipeline for the [EMNIST Letters](https://www.nist.gov/itl/products-and-services/emnist-dataset) dataset (A–Z).

- **LICENSE**  
  Licensed under the **Apache License 2.0**.

- **README.md**  
  This file.

---

## 🚀 Features

- **Boundary extraction** using Canny edges (or morphological gradient as fallback).
- **Central-difference gradients** (gx, gy) with optional **gradient magnitude**.
- **Masked gradient features** → model focuses on strokes and contours.
- **Global feature standardization** for stable MLP training.
- **Multi-layer Perceptron classifier** with BatchNorm, Dropout, and LeakyReLU.
- **Callbacks** for early stopping and learning-rate scheduling.

---

## 📊 Results (baseline)

- **MNIST Digits**:  
  > Accuracy ~98–99% with 3-channel gradient features.  
- **EMNIST Letters**:  
  > Accuracy ~88–92% (letters are more challenging).

(Exact results may vary depending on training parameters and hardware.)

---

## 🔧 Usage

Clone this repository and open the notebooks in **Google Colab** or locally with Jupyter:

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
