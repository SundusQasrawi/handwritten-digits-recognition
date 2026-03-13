# Handwritten Arabic Digit Recognition using CNN

This project implements a deep learning system for recognizing handwritten Arabic digits (0–9) using a Convolutional Neural Network (CNN). The model learns visual features directly from images and predicts the corresponding digit class.

The project was developed as part of a Computer Vision course at Birzeit University.

## Overview

Handwritten digit recognition is an important computer vision task used in document processing, automated form reading, and digital archiving. Recognizing handwritten Arabic digits is challenging because handwriting styles vary widely between individuals.

In this project, a CNN-based model is trained to classify handwritten Arabic numerals using grayscale image inputs.

## Model Architecture

The proposed CNN consists of two convolutional blocks followed by fully connected layers:

- Conv (3×3, 32 filters) + BatchNorm + ReLU  
- Conv (3×3, 32 filters) + BatchNorm + ReLU  
- MaxPool (2×2)  
- Conv (3×3, 64 filters) + BatchNorm + ReLU  
- Conv (3×3, 64 filters) + BatchNorm + ReLU  
- MaxPool (2×2)  
- Flatten  
- Dense (128) + ReLU  
- Dense (10) + Softmax  

Batch normalization improves training stability and helps the model generalize better.

## Dataset

The model is trained on the **Handwritten Arabic Numerals Dataset**, which contains:

- 9350 grayscale images
- 10 digit classes (0–9)
- Image resolution: 28×28 pixels

The dataset is split into:
- 70% training
- 15% validation
- 15% testing

## Preprocessing and Augmentation

Images are preprocessed by:

- resizing to 28×28 pixels  
- normalizing pixel values to [0,1]  
- applying image inversion  

To improve generalization, data augmentation is applied during training:

- small rotations
- horizontal and vertical shifts
- zoom transformations

## Results

Experiments were conducted to study the effects of architecture design, regularization, and data augmentation. The final model achieved:

- **Accuracy:** 97.29%
- **Precision:** 97.35%
- **Recall:** 97.29%
- **F1-score:** 97.29%

The results show that a lightweight CNN architecture can achieve high performance on handwritten Arabic digit recognition.


## Technologies

Python, TensorFlow, NumPy, OpenCV, Matplotlib, Jupyter Notebook

