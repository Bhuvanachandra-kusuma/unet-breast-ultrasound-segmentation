# U-Net Breast Ultrasound Tumor Segmentation (BUSI Dataset)

## Overview

This repository implements a U-Net convolutional neural network for pixel-wise tumor segmentation in breast ultrasound images.

The model is trained and evaluated on the BUSI (Breast Ultrasound Images) dataset using a composite Binary Cross-Entropy + Dice loss to address class imbalance. Performance is measured using Dice coefficient and Intersection-over-Union (IoU).

This project was developed as preparation for integrating deep learning segmentation with physics-based ultrasound inverse modeling workflows.

---

## Dataset

**Breast Ultrasound Images (BUSI) Dataset**

- Total Images: 780 grayscale ultrasound images  
- Classes: benign, malignant, normal  
- Ground-truth segmentation masks provided  
- Training performed on benign + malignant samples  

Dataset source:  
https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset

Original publication:
Al-Dhabyani et al., “Dataset of breast ultrasound images,” Data in Brief, 2020.

---

## Model Architecture

- Encoder–decoder U-Net architecture  
- Skip connections between contracting and expanding paths  
- Batch Normalization layers  
- Sigmoid activation for binary segmentation  

Input size: 128 × 128 grayscale images  

---

## Loss Function

To mitigate severe class imbalance in ultrasound tumor segmentation, a composite loss was used:

Binary Cross-Entropy + Dice Loss

This stabilizes early training and improves boundary detection accuracy.

---

## Results

Segmentation performance on tumor images:

- Dice Coefficient: 0.91  
- IoU (Jaccard Index): 0.89  

These results demonstrate strong spatial overlap between predicted and ground-truth tumor boundaries.

---

## Technologies Used

- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  

