# Fight/Violence Detection in Videos Using 3D CNN

This repository contains a dataset and a 3D CNN (Convolutional Neural Network) model trained to detect fights/violence and non-violence in videos. The model is designed to capture temporal and spatial features to identify violent activities, making it suitable for real-time surveillance and security applications.

## Dataset Overview

- **Dataset Classes:** The dataset consists of two classes:
  1. **Violence/Fight:** Videos where physical violence is present.
  2. **NoViolence/NoFight:** Videos with no physical confrontations.
  
- **Data Format:**
  - The dataset contains videos that are labeled into the above two classes.
  - These videos are preprocessed and split into frames that are fed into the 3D CNN model for training and detection.

## Model

- **3D CNN Architecture:**
  - The 3D CNN model is trained to detect patterns across both spatial and temporal dimensions, making it ideal for analyzing video sequences.
  - The model uses 3D convolutional layers to capture motion and action-based features, which are crucial for fight/violence detection.

## Purpose

The model is developed to detect violent actions in video footage. This system can be deployed in surveillance cameras, security systems, or any environment where fight/violence detection is necessary.

### Key Features:
- **Fight/Violence Detection:**
  - The 3D CNN model is trained to recognize fight/violence events in videos, differentiating them from non-violent actions.
  - The model processes video sequences to make predictions, utilizing temporal changes and spatial context.

## Code and Usage Instructions

### Pre-requisites:
- Python 3.8 or higher
- TensorFlow or PyTorch (depending on the implementation)
- OpenCV
- FFmpeg (for video preprocessing)
- Required libraries as mentioned in `requirements.txt`

### Video Preprocessing:

1. **Extract Frames from Video:**
   The 3D CNN model expects the input as video frames. You can extract frames from videos using the following command:
   
   ```bash
   ffmpeg -i <input-video> -vf fps=25 <output-frame-directory>/frame_%04d.jpg
