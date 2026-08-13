# Task 2 — Senior Citizen Identification

## VGG16 Age + Gender Model

This project detects people from images, videos, and webcam input and predicts:

- Age
- Gender
- Senior citizen status

A person is classified as a **Senior Citizen when the predicted age is greater than 60**.

## Model Architecture

The project uses a VGG16-based multi-output neural network:

- VGG16 with ImageNet weights
- Input size: 224 × 224 × 3
- Frozen VGG16 backbone
- Data augmentation
- Flatten layer
- Shared Dropout(0.30)
- Separate age and gender branches
- Two Dense(512) layers in each branch
- Batch Normalization
- Dropout
- Age output: Linear regression
- Gender output: Sigmoid binary classification

## Dataset

The model is designed for a 10,000-image dataset:

- 5,000 senior images
- 5,000 non-senior images
- Total: 10,000 images

The dataset is not included in this repository.

## Features

- Age prediction
- Gender prediction
- Senior citizen identification
- Multiple face detection
- Image processing
- Video processing
- Real-time webcam detection
- Person tracking
- Visit logging
- CSV logging
- Excel export
- Tkinter GUI

## Face Detection

OpenCV YuNet is used only for detecting and locating faces.

The VGG16 model is responsible for age and gender prediction.

The YuNet model file should be placed at:

```text
models/
└── face_detector/
    └── face_detection_yunet_2023mar.onnx
