# ISIC 2024 Lesion Segmentation

## Overview

This project implements a deep learning-based approach for the **ISIC 2024 Challenge**, focusing on the task of **skin lesion segmentation from dermoscopic images**.

The goal is to support the early detection of skin cancer by developing an automated system capable of accurately segmenting lesions from skin images using a convolutional neural network.

Skin cancer is one of the most common types of cancer, and early detection significantly improves treatment outcomes. Dermatologists use dermoscopic images to identify abnormal skin lesions, but this process can be time-consuming and subjective.

Automated image segmentation methods can assist medical professionals by highlighting regions of interest that may require further investigation.

This project applies deep learning techniques to perform **semantic segmentation of skin lesions** using the **U-Net architecture**, which is widely used for biomedical image segmentation tasks.

---

## Dataset

The dataset used in this project is provided by the **International Skin Imaging Collaboration (ISIC)** as part of the ISIC Challenge.

It consists of:

- High-quality dermoscopic images  
- Ground truth segmentation masks identifying lesion boundaries  

You can download the dataset by registering on the ISIC Challenge website:

https://challenge.isic-archive.com/data/#2018

After downloading, the images and their corresponding masks should be organized into an appropriate folder structure for model training and validation.

---

## Approach

The project follows a typical deep learning workflow for medical image segmentation.

Key steps include:

- Loading and preprocessing dermoscopic images and corresponding ground truth masks  
- Image preprocessing such as resizing, normalization, and data augmentation  
- Implementing and training a **U-Net convolutional neural network** using the **Keras deep learning framework**  
- Generating **binary segmentation masks** that highlight lesion regions  

### Model Architecture

The **U-Net architecture** is used for segmentation. It is a fully convolutional network designed specifically for biomedical image segmentation.

The architecture consists of:

- A **contracting path** that captures contextual information  
- A **symmetric expanding path** that enables precise localization  

This design allows the model to learn high-resolution spatial features that are essential for accurate lesion boundary detection.

---

## Results

The model was trained on a subset of the ISIC dataset with data augmentation techniques to increase dataset diversity and improve generalization.

Model performance was evaluated using commonly used segmentation metrics:

- **Dice Coefficient**
- **Intersection over Union (IoU)**

Visual comparisons between predicted masks and ground truth masks demonstrate the model’s ability to accurately segment lesion regions.

---

## Example Output

Example predicted segmentation masks highlighting lesion areas in dermoscopic images.

*(Add prediction images here to visualize the segmentation results.)*

---

## Tech Stack

- Python  
- Keras / TensorFlow  
- NumPy  
- OpenCV  

---

## Future Work

Potential improvements for future versions of this project include:

- Hyperparameter tuning (learning rate, batch size, number of epochs)  
- Incorporating a **pre-trained encoder** such as ResNet or EfficientNet within a U-Net variant  
- Expanding the dataset to improve model generalization  
- Deploying the model as a **web application using Streamlit or Flask** for interactive visualization and experimentation
