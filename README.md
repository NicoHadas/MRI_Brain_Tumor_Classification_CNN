# MRI Brain Tumor Classification using Convolutional Neural Networks (CNN)

## Overview
This repository contains the code for a Convolutional Neural Network (CNN) model developed to perform multi-class classification of brain tumors from Magnetic Resonance Imaging (MRI) data. Brain tumors represent a significant health challenge, and early, accurate detection is vital for patient outcomes. This project aims to demonstrate the potential of deep learning to automate and improve the accuracy of brain tumor classification, supporting diagnostic workflows.

---

## Data Source
-   **Kaggle Dataset**: The model was trained and evaluated using a public dataset from Kaggle, comprising 3264 MRI images.
    -   **Link to dataset**: [Brain Tumor MRI Dataset Kaggle]([https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset])
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
    * 3264 MRI images were obtained from the public Kaggle dataset.
    * Images were resized to 150x150 pixels for uniformity.
    * Labels were numerically encoded (glioma = 0, meningioma = 1, pituitary = 2, no tumor = 3).
    * Image pixel values were normalized to a range of \[0, 1].
    * Data was converted to PyTorch tensors.
2.  **Data Splitting**:
    * The dataset was divided into training (80%) and testing (20%) sets.
    * PyTorch `TensorDataset` and `DataLoader` objects were used for batch processing and shuffling of training data.
3.  **Model Architecture**:
    * A CNN was designed with:
        * Three convolutional layers (producing 16, 32, and 64 feature maps respectively).
        * Each convolutional layer was followed by a ReLU activation function and a max-pooling operation.
        * Two fully connected layers.
        * The final output layer had four units, corresponding to the four classes.
4.  **Model Training**:
    * The model was trained for 10 epochs.
    * Cross-entropy loss function was used.
    * Adam optimizer was employed for updating model weights via backpropagation.
    * Training progress was monitored by loss and accuracy metrics.
5.  **Model Evaluation**:
    * Performance was assessed on the test dataset using:
        * Overall accuracy
        * Confusion matrix
        * Per-class precision, recall, and F1-score
        * Receiver Operating Characteristic (ROC) curves and Area Under the Curve (AUC) for each class.

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
    * **Pituitary Tumor**: Achieved exceptional performance with an F1-score of 0.99.
    * **No Tumor**: Effectively distinguished with a recall of 0.87, despite having the fewest samples in the test set.
    * **Meningioma Tumor**: F1-Score: 0.87
    * **Glioma Tumor**: F1-Score: 0.88
* **ROC Curves**: High AUC values were reported across all four classes, indicating robust discriminatory power.
* **Confusion Matrix**: Showed good class separation.

These findings suggest that the CNN model can provide rapid, consistent, and accurate brain tumor classification, highlighting its potential as an AI-assisted tool in radiology.

---
