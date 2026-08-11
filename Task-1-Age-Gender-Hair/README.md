cat > Task-1-Age-Gender-Hair/README.md <<'EOF'
# Task 1 — Age, Gender & Hair Length Detection

## Overview

This project implements a computer vision system for age prediction, gender prediction, and hair-length classification.

The system combines two CNN models:

- VGG16 for age and gender prediction
- EfficientNetB0 for hair-length classification

A rule-based logic is applied to the final prediction for people aged 20–30 according to the task requirements.

## Models

### Age and Gender

VGG16 pretrained on ImageNet is used as the CNN backbone.

The model has two branches:

- Age: regression with a linear output
- Gender: binary classification with a sigmoid output

Dropout, data augmentation, early stopping, learning-rate reduction, and fine-tuning are used during training.

### Hair Length

EfficientNetB0 pretrained on ImageNet is used for:

- Long Hair
- Short Hair

## Dataset

The project uses the UTKFace dataset for age and gender prediction and a separate hair-length dataset for hair classification.

The datasets are not included in this repository because of their size.

## Special Rule

For people aged between 20 and 30, hair length is incorporated into the required gender-prediction logic.

For people outside this age range, the normal gender prediction is retained.

## Project Structure

```text
Task-1-Age-Gender-Hair/
├── notebook/
│   └── age_gender_hair_VGG16_FINAL.ipynb
├── app/
├── models/
├── README.md
└── requirements.txt
