# Tree Species Classification

A computer vision project developed during an **EduNet Internship** to classify tree species from images using deep learning.

## Project Overview

This project focuses on building an image classification pipeline for identifying different tree species from a labeled image dataset.

The workflow includes dataset inspection, data cleaning, preprocessing, image augmentation, model training, and experimentation with different convolutional neural network architectures.

## Dataset

* **Initial dataset:** 1,605 images across 31 tree species
* Duplicate images were identified and removed.
* Corrupted images were detected and removed.
* Image-dimension outliers were analyzed and removed.
* **Cleaned dataset:** 1,454 images
* Images were resized to **224 × 224 pixels**.
* An **80/20 training-validation split** was used.

## Data Preprocessing

The preprocessing pipeline included:

* Duplicate image detection
* Corrupted image detection
* Image-dimension analysis
* Outlier removal
* Image resizing
* Pixel-value rescaling
* Data augmentation

Augmentation techniques included:

* Rotation
* Zoom
* Shearing
* Horizontal flipping

## Models Explored

### 1. Basic CNN

A convolutional neural network was developed using multiple:

* Convolution layers
* Max-pooling layers
* Fully connected layers
* Dropout

The model was trained for multi-class tree species classification.

### 2. EfficientNetB0 Transfer Learning

An **ImageNet-pretrained EfficientNetB0** model was also explored.

The pretrained base was initially frozen and combined with:

* Global Average Pooling
* Dense layer
* Dropout
* Softmax output layer for 31 classes

### 3. Improved CNN Experiment

An additional CNN configuration was explored using:

* Batch Normalization
* Dropout
* Early Stopping
* Reduce Learning Rate on Plateau

These experiments were used to compare different approaches to the classification problem.

## Project Workflow

```text
Raw Image Dataset
        ↓
Dataset Inspection
        ↓
Duplicate Detection
        ↓
Corrupted Image Detection
        ↓
Outlier Analysis
        ↓
Data Cleaning
        ↓
Image Resizing & Rescaling
        ↓
Data Augmentation
        ↓
Train / Validation Split
        ↓
Model Training
   ┌───────────────┐
   ↓               ↓
Basic CNN     EfficientNetB0
   │               │
   └───────┬───────┘
           ↓
     Model Experiments
```

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Seaborn
* OpenCV
* Scikit-learn
* Google Colab

## Repository Structure

```text
tree-species-classification/
│
├── README.md
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_model_training.ipynb
│   └── 03_model_experiments.ipynb
│
├── models/
│   └── trained_models/
│
├── results/
│   └── training_results/
│
└── requirements.txt
```

> The notebook names and folder structure may be adjusted according to the final organization of the original notebooks.

## Key Work

* Cleaned and prepared a multi-class image dataset containing 31 tree species.
* Identified and removed duplicate and corrupted images.
* Performed image-dimension and outlier analysis.
* Applied image preprocessing and augmentation techniques.
* Implemented a CNN-based image classification model.
* Experimented with EfficientNetB0 transfer learning.
* Compared different model-training configurations and regularization techniques.

## Internship Context

This project was completed as part of an **EduNet Internship** and provided practical experience in:

* Data preprocessing
* Computer vision
* Image classification
* Deep learning
* Transfer learning
* Model experimentation
* Dataset analysis

## Future Improvements

Possible improvements include:

* Increasing the size and diversity of the dataset
* Further hyperparameter tuning
* Exploring additional pretrained architectures
* Improving class balance
* Evaluating the models using precision, recall, F1-score, and confusion matrices
* Deploying the best-performing model as an inference application
