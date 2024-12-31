# MNIST Handwritten Digit Classification with LeNet-5

This project implements the **LeNet-5** Convolutional Neural Network (CNN) architecture using **PyTorch** to classify handwritten digits from the **MNIST dataset**. The model achieves high accuracy and demonstrates effective generalization without overfitting.

## Overview
LeNet-5, introduced by Yann LeCun in 1998, is a CNN designed for image classification tasks. It consists of:
- Three convolutional layers for feature extraction.
- Two average pooling layers to reduce spatial dimensions.
- Two fully connected layers ending with a SoftMax classifier.

The architecture is adapted to classify digits (0–9) from the MNIST dataset.

## Dataset
- **MNIST Training Set**: 60,000 images and labels (`mnist_train.csv`).
- **MNIST Test Set**: 10,000 images and labels (`mnist_test.csv`).
- Each row consists of 785 values: the first value is the label, and the remaining 784 are pixel values of the 28x28 grayscale image.

## Implementation Steps
1. **Data Preparation**:
   - Loaded MNIST datasets from CSV files.
   - Resized images from 28x28 to 32x32 to match LeNet-5 input requirements.
   - Normalized pixel values to [0,1] and converted data to PyTorch tensors.

2. **LeNet-5 Model**:
   - Implemented the original architecture in PyTorch.
   - Used tanh activation for convolutional layers and SoftMax for classification.

3. **Training and Validation**:
   - Optimized with Adam optimizer and CrossEntropy loss.
   - Monitored accuracy and loss per epoch for both training and validation sets.

4. **Evaluation**:
   - Tested on the MNIST test set, achieving **98.47% accuracy**.
   - Confusion matrix visualized to analyze misclassifications.

## Results
- **Training Accuracy**: Reached 99.16% after 10 epochs.
- **Validation Accuracy**: Reached 98.50%, closely aligned with training accuracy.
- **Test Accuracy**: Achieved a final accuracy of 98.47%, indicating excellent generalization.

### Key Insights:
- The model converges rapidly due to LeNet-5’s suitability for MNIST’s simple structure.
- Minimal difference between training and validation metrics demonstrates no overfitting.
- Effective use of tanh activation and pooling layers enhances performance.

## Challenges
1. **Resizing Input Images**:
   - Adapting 28x28 images to 32x32 required careful handling to preserve spatial features.
2. **Hyperparameter Tuning**:
   - Achieved optimal results with a learning rate of 0.001 and batch size of 64.

## Visualizations
- Plotted training and validation accuracy over epochs.
- Confusion matrix displayed class-wise predictions, highlighting areas of improvement.

## Conclusion
LeNet-5’s performance on the MNIST dataset demonstrates its robustness as a baseline model for digit classification tasks. With a test accuracy of 98.47%, the model is well-suited for generalization and efficient learning.
