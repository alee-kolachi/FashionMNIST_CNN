# FashionMISTModelV1 — Fashion-MNIST (PyTorch + Colab)

This project implements a simple CNN (`FashionMISTModelV1`) in PyTorch to classify images from the [Fashion-MNIST dataset](https://github.com/zalandoresearch/fashion-mnist).  
The code is designed to run in **Google Colab** with minimal setup.

---

## Model architecture

`FashionMISTModelV1` consists of:
- **2 convolutional blocks**: Conv → ReLU → Conv → ReLU → MaxPool  
- **1×1 conv head** reducing channels to 10  
- **Linear classifier** (`10*7*7 → 10`)  

Loss: `CrossEntropyLoss`  
Optimizer: `Adam (lr=1e-3)`

---

## Training / Evaluation Flow

1. Train for a few epochs on Fashion-MNIST (train + val split).
2. Evaluate on validation and test sets.
3. Visualize predictions for random samples from the test set.

---

## Requirements

Install the following in Colab (or locally):

```bash
pip install torch torchvision matplotlib tqdm
