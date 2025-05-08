# ISIC 2024 Lesion Segmentation

This repository contains a deep learning-based approach to the ISIC 2024 Challenge, specifically focused on the task of skin lesion segmentation from dermoscopic images. The project is designed to support the early detection of skin cancer by developing an automated system that can accurately segment lesions from skin images using a convolutional neural network.

## Project Description

Skin cancer is one of the most common types of cancer, and early detection plays a crucial role in improving treatment outcomes. Dermatologists use dermoscopic images to identify abnormal skin lesions, but the process can be time-consuming and subjective. Automated image segmentation methods can assist medical professionals by highlighting regions of interest that may require further investigation.

In this project, we apply deep learning techniques to perform semantic segmentation of skin lesions. The core of this implementation is the U-Net architecture, which is known for its effectiveness in biomedical image segmentation tasks. The model takes dermoscopic images as input and outputs binary masks that highlight the lesion regions.

## Objectives

1. Load and preprocess the ISIC 2024 dataset, including dermoscopic images and their corresponding ground truth masks.
2. Perform image preprocessing such as resizing, normalization, and data augmentation to improve generalization.
3. Implement and train a U-Net model using the Keras deep learning framework.
4. Evaluate model performance using appropriate metrics such as Dice coefficient and Intersection over Union.
5. Visualize and analyze the results by comparing predicted masks with ground truth masks.

## Dataset

The dataset used in this project is provided by the International Skin Imaging Collaboration (ISIC) as part of the 2024 challenge. It consists of high-quality dermoscopic images along with manually annotated masks that identify lesion boundaries.

You can download the dataset by registering on the ISIC Challenge website at:

https://challenge.isic-archive.com/data/#2018

After downloading, the images and their corresponding masks should be organized into a folder structure suitable for training and validation.


## Model Architecture

The U-Net architecture is used in this project. It is a fully convolutional network designed specifically for biomedical image segmentation. It consists of a contracting path that captures context and a symmetric expanding path that enables precise localization. This design allows the network to learn high-resolution features that are critical for accurate segmentation.

## Results and Evaluation

The model was trained on a subset of the ISIC dataset with data augmentation techniques to increase diversity. The evaluation metrics used include the Dice coefficient and Intersection over Union (IoU), both of which are standard in image segmentation tasks.

The results demonstrate the model's ability to accurately segment lesion areas, with visual comparisons showing strong overlap between predicted and ground truth masks.

## Future Work

Some possible improvements for future iterations of the project include:

- Fine-tuning hyperparameters such as learning rate, batch size, and number of epochs.
- Incorporating a pre-trained encoder (for example, ResNet or EfficientNet) as part of a U-Net variant.
- Expanding the dataset for better generalization.
- Deploying the model as a web application using Streamlit or Flask for interactive use.
