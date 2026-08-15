# Task 3 - Audio Analysis

## Overview

This project analyzes speech audio and predicts:

- Age
- Gender
- Senior Citizen status
- Emotion

## Features

- Upload WAV / MP3 audio
- Play audio
- Stop audio
- Analyze audio
- Predict age
- Predict gender
- Detect senior citizen
- Predict emotion
- Interactive GUI

## Datasets

### Common Voice
Used for age and gender prediction.

### RAVDESS
Used for speech emotion recognition.

The datasets are not included in this repository because of their large size.

## Models

The trained models are included in the `models` folder:

- `age_gender_audio_model.keras`
- `senior_gender_audio_model.keras`
- `emotion_audio_model.keras`
- `age_norm_stats.npy`
- `senior_threshold.npy`

## Technologies

- Python
- TensorFlow / Keras
- Librosa
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Tkinter
- Jupyter Notebook

## Installation

Install the required packages:

```bash
pip install -r requirements.txt
