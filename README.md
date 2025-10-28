# MRI Brain Tumor Classification using Convolutional Neural Networks (CNN)

## Overview
This repository contains the code for a Convolutional Neural Network (CNN) model developed to perform multi-class classification of brain tumors from Magnetic Resonance Imaging (MRI) data. Data was obtained with Kaggle

---

## Data Source
-   **Kaggle Dataset**: The model was trained and evaluated using a public dataset from Kaggle, comprising 3264 MRI images.
    -   **Link to dataset**: [Brain Tumor MRI Dataset Kaggle](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
    -   **Classes**: The images are categorized into four classes:
        1.  Glioma Tumor
        2.  Meningioma Tumor
        3.  Pituitary Tumor
        4.  No Tumor
    -   **Dataset Composition**:
        * Meningioma Tumor: 937 images
        * Glioma Tumor: 926 images
        * Pituitary Tumor: 901 images
        * No Tumor: 500 images

---

## Repository Structure

-   **/Python**
    -   `CNN.ipynb`: Jupyter notebook containing all Python code for data preprocessing, model architecture definition, training, evaluation, and visualization of results.

---

## Methods Summary

A Convolutional Neural Network (CNN) was developed and evaluated for the automated multi-class classification of brain tumors.

1.  **Data Collection and Preprocessing**:
    * 3264 MRI images obtained from the Kaggle dataset.
    * Images were normalized and converted to tensors.
2.  **Data Splitting**:
    * Training (80%) and Testing (20%).
3.  **Model Architecture**:
    * Three convolutional layers (producing 16, 32, and 64 feature maps respectively).
    * Each convolutional layer followed by ReLU activation function and max-pooling operation.
    *Two fully connected layers.
    *The final output layer had four units, corresponding to the four classes.
4.  **Model Training**:
    * Model was trained for 10 epoch using Cross-entropy loss and Adam optimizer
5.  **Model Evaluation**:

---

## Results Summary

The trained CNN demonstrated high accuracy in classifying brain tumors from MRI images.

* **Overall Performance (Test Set)**:
    * Accuracy: 90%
    * Macro Average Precision: 0.90
    * Macro Average Recall: 0.89
    * Macro Average F1-Score: 0.90
    * Weighted Average Precision: 0.90
    * Weighted Average Recall: 0.90
    * Weighted Average F1-Score: 0.90
* **Per-Class Performance Highlights**:
    * **Pituitary Tumor**: Achieved exceptional performance with F1-score of 0.99.
    * **No Tumor**: Effectively distinguished with a recall of 0.87, despite having the fewest samples in test set.
    * **Meningioma Tumor**: F1-Score: 0.87
    * **Glioma Tumor**: F1-Score: 0.88
* **ROC Curves**: High AUC values were reported across all four classes.
* **Confusion Matrix**: Good class separation.

---
