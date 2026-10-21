
# Laboratory Activity 2: Neural Network Image Recognition

## Overview

This laboratory activity explores image classification using a simple dense neural network trained on the Butterfly Image Classification dataset.

The experiment compares the model's performance using different image resolutions: 32 × 32, 64 × 64, and 128 × 128 pixels.

## Objectives

- Prepare and split an image-classification dataset.
- Build and train a dense neural network.
- Compare training time and test accuracy across image resolutions.
- Evaluate classification performance.
- Identify the limitations of a simple neural network for image recognition.

## Dataset

**Dataset:** [Butterfly Image Classification](https://www.kaggle.com/datasets/phucthaiv02/butterfly-image-classification)

- Total labeled images: 6,499
- Number of classes: 75
- Data split: approximately 70% training, 15% validation, and 15% testing
- Splitting approach: stratified

## Technologies Used

- Python
- TensorFlow/Keras
- NumPy
- scikit-learn
- Matplotlib
- Google Colab
- Jupyter Notebook

## Model Architecture

The experiment uses a simple dense neural network with the following architecture:

1. **Flatten:** Converts the image into a one-dimensional vector.
2. **Dense layer:** 128 units with ReLU activation.
3. **Output layer:** 75 units with softmax activation.

### Training Configuration

- Optimizer: Adam
- Loss function: Sparse categorical cross-entropy
- Batch size: 32
- Epochs: 10
- Image resolutions: 32 × 32, 64 × 64, and 128 × 128

## Experimental Results

| Image Resolution | Test Accuracy | Training Time |
|---|---:|---:|
| 32 × 32 | 19.59% | 15.14 seconds |
| 64 × 64 | 6.67% | 42.51 seconds |
| 128 × 128 | 1.95% | 171.60 seconds |

*Values are based on the reported experimental results.*

## Analysis

The 32 × 32 configuration achieved the highest test accuracy among the three experiments. Increasing the image resolution increased training time but did not improve classification performance.

The results demonstrate that image resolution alone does not guarantee better accuracy. A flattened dense neural network may struggle to capture spatial patterns and visual features that distinguish similar butterfly species.

The report also recorded different class-level F1-scores, including:

- ULYSES: 0.7333
- AMERICAN SNOOT: 0.0000

These results indicate that performance varied considerably across classes.

## Conclusion

This activity demonstrates the process of training and evaluating a neural network for image classification. It also highlights the importance of model architecture, dataset characteristics, and evaluation metrics when developing image-recognition systems.

A possible improvement is to experiment with convolutional neural networks (CNNs), which are designed to learn spatial features from images.

## Author

**Renna M. Israel**
