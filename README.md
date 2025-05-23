# Semi-Supervised-_Learning_for_Image_Classification
Semi-Supervised Image Classification on MNIST with UDA (PyTorch) . Using only 100 labeled examples, the method achieves an accuracy of 0.97.
# 🧠 Semi-Supervised Image Classification on MNIST with UDA (PyTorch)

This project implements **Unsupervised Data Augmentation (UDA)** for semi-supervised learning on the **MNIST** dataset using **PyTorch**. UDA improves classification performance by enforcing consistency between predictions on original and strongly augmented unlabeled data — enabling high accuracy even with very limited labeled samples.

> Based on the paper:  
> *Xie, Qizhe, et al. “Unsupervised Data Augmentation for Consistency Training.” NeurIPS 2020*  
> [Link to paper](https://arxiv.org/abs/1904.12848)

## 🎯 Objectives

- Train an image classifier using only **100 labeled samples**
- Leverage the remaining **unlabeled MNIST images** through UDA
- Compare against a fully supervised baseline trained on the same 100 examples

## 🧪 Dataset

- **Dataset**: MNIST (handwritten digit classification, 28×28 grayscale)
- **Labeled training set**: 100 samples randomly selected
- **Unlabeled training set**: remaining training images (59,900)
- **Test set**: standard MNIST test split (10,000 samples)

## 🛠️ Methods & Tools

- **Framework**: PyTorch
- **UDA Components**:
  - Weak/strong augmentations (rotation, crop, noise)
  - Consistency loss with confidence-based pseudo-labeling
  - Thresholding to select reliable pseudo-labels
- **Model**: Convolutional Neural Network (CNN)

## 📈 Results

UDA significantly improves performance compared to supervised learning with only 100 labeled samples.

| Model            | # Labeled Samples | Test Accuracy |
|------------------|-------------------|----------------|
| Supervised CNN   | 100               |  79%   |
| CNN + UDA (Ours) | 100 + unlabeled   |  97%   |
