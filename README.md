# Polyp Detection with DETR

## Introduction

Polyp detection in colonoscopic images is a complex challenge that has been addressed through various computer-aided systems over the years. Due to the varying sizes and diverse appearances of polyps, coupled with differing detection techniques and clinical opinions, achieving high accuracy in detection is crucial. This project utilizes the DETR (Detection Transformer) model, which incorporates modern neural network architectures for object detection to enhance accuracy and reduce diagnosis times.

## Project Objective

Our goal is to develop a model that not only performs object detection in a single step but also incorporates self-attention mechanisms to improve detection accuracy. This approach allows the model to selectively focus on different parts of an image, enhancing its ability to discern and differentiate objects effectively.

## Key Features

- **High Accuracy:** Leverages the self-attention mechanism to dynamically prioritize relevant features within the image, leading to precise detection outcomes.
- **Efficient Detection:** Streamlines the object detection process by reducing computational complexity, thus improving overall system efficiency.
- **Advanced Integration:** Uses datasets sourced from Roboflow and pretrained models from Hugging Face to ensure robust and scalable detection performance.

## Model Overview

### Self-Attention in DETR

The DETR model integrates a transformer-based encoder-decoder architecture that employs self-attention to capture spatial relationships and contextual information, enabling the model to process images holistically. This capability is particularly beneficial in medical imaging, where understanding the full context of an image is crucial.

### Components of DETR

1. **CNN Backbone:** Extracts initial features from the input images.
2. **Encoder-Decoder Transformer:** Utilizes self-attention to enhance the interpretative accuracy of the model.
3. **Feed-Forward Network (FFN):** Determines the object classes and their bounding boxes from the transformer's output.

### Hungarian Algorithm

The model uses the Hungarian algorithm to match detected objects with ground truth annotations efficiently, facilitating one-step object detection without the need for multiple processing stages.

## Repository Structure

```plaintext
├── data                    # Dataset files
├── models                  # Trained models and model definitions
├── notebooks               # Jupyter notebooks for demonstrations and testing
├── src                     # Source code for training and inference
├── tests                   # Test cases for automated testing of the code
├── LICENSE
└── README.md
