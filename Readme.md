
# A Novel Deep Learning-Based Multi-Model Decision Fusion System for the Classification of Naga Traditional Shawls

## Overview

This project presents a deep learning-based image classification system for identifying and classifying traditional Naga shawls from images.

The proposed system employs a **multi-model decision fusion approach**, combining the predictions of multiple deep learning models to improve classification performance. The system is designed to address the challenges associated with the visual similarity, complex patterns, colors, and textures found in traditional Naga shawls.

The project is part of an ongoing research study and is intended to contribute to the digital documentation, recognition, and preservation of traditional Naga textile heritage.

## Objectives

- To develop an automated image-based classification system for traditional Naga shawls.
- To investigate the effectiveness of deep learning models for Naga shawl classification.
- To develop a multi-model decision fusion approach for improving classification performance.
- To compare the performance of individual deep learning models with the proposed fusion approach.
- To evaluate the system using standard classification performance metrics.
- To support the digital documentation and preservation of traditional Naga textile heritage.

## Proposed Methodology

The system follows the following workflow:

1. Dataset Collection
2. Image Preprocessing
3. Data Augmentation
4. Dataset Splitting
5. Individual Model Training
6. Feature/Prediction Extraction
7. Multi-Model Decision Fusion
8. Final Classification
9. Performance Evaluation

## Deep Learning Models

The proposed system uses multiple deep learning models for image classification.

The individual models generate probability distributions for the different shawl classes. These predictions are then combined using a **decision fusion strategy** to obtain the final classification result.

### The models used in the current implementation include:

- Custom CNN
- MobileNetV2
- ResNet

The specific models and experimental configurations may be updated as the research progresses.

## Decision Fusion

The proposed system uses *soft decision fusion (probability averaging)*

Each individual model produces a probability distribution across the available shawl classes. The prediction probabilities from the models are combined to obtain a final probability distribution.

The class with the highest combined probability is selected as the final prediction.

## Conceptually:

```text
Input Image
     │
     ├──> Custom CNN ───> Class Probabilities ──┐
     │                                          │
     ├──> MobileNetV2 ─> Class Probabilities ──┼──> Decision Fusion
     │                                          │
     └──> ResNet ──────> Class Probabilities ──┘
                                                    │
                                                    ▼
                                             Final Prediction
