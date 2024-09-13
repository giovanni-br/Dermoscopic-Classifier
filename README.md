# Skin Lesion Classification

### Giovanni Benedetti Da Rosa  
📅 **Date**: May 5, 2024

## Introduction

This repository contains the code, report, and other resources for the final challenge of the IMA205 course at Télécom Paris. The project focuses on classifying dermoscopic images of skin lesions into eight diagnostic categories using machine learning techniques, including Convolutional Neural Networks (CNNs) and traditional machine learning models. The dataset used for this challenge is derived from the ISIC (International Skin Imaging Collaboration) dataset.

For detailed methodology, results, and analysis, refer to the [**Final Report**](https://github.com/giovanni-br/Dermoscopic-Classifier/blob/main/Report_IMA205%20(2).pdf).
![skin_lesion](https://github.com/user-attachments/assets/a8b095de-5f6b-4b57-9dcf-2d02d6d42e47)

## Dataset

The dataset provided for this challenge includes 25,331 dermoscopic images, divided into training, validation, and test sets. The training-validation set contains 18,998 images, while the remaining 6,333 images make up the test set.

**Classes in the dataset:**
1. Melanoma
2. Melanocytic nevus
3. Basal cell carcinoma
4. Actinic keratosis
5. Benign keratosis
6. Dermatofibroma
7. Vascular lesion
8. Squamous cell carcinoma

Additional metadata (e.g., age, gender, lesion location) was provided, which was used for further data analysis and preprocessing.

## Methods

Two approaches were employed to classify the skin lesions:

1. **Feature-based Classification**:
    - Segment the lesion and extract features based on the ABCD criteria (Asymmetry, Border irregularity, Color variation, and Diameter).
    - Machine learning models such as Random Forest, SVM, and MLP were used for classification.

2. **CNN-based Classification (ResNet)**:
    - Used a ResNet101 model, known for its success in image classification tasks.
    - Images were resized to 224x224, and data augmentation techniques were applied to improve model performance.

## Results

| Method           | Validation Accuracy | Public Test Accuracy | Private Test Accuracy |
|------------------|---------------------|----------------------|-----------------------|
| SVM              | 0.64                | 0.38                 | 0.36                  |
| Random Forest    | 0.62                | 0.40                 | 0.38                  |
| MLP              | 0.57                | 0.38                 | 0.36                  |
| **ResNet101**    | **0.76**            | **0.67**             | **0.63**              |

ResNet101 outperformed the feature-based models in this task, demonstrating the strength of deep learning methods in handling complex image classification problems.
