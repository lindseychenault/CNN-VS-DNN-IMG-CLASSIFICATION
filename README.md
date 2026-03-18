# CNN vs Dense Neural Networks: Architecture, Depth, and Regularization in Image Classification

## Overview
This project investigates how neural network architecture, depth, and regularization impact performance and generalization in image classification tasks.

Using the CIFAR-10 dataset, this study compares fully connected neural networks (DNNs) and convolutional neural networks (CNNs) under controlled experimental conditions.

## Objective
- Compare CNNs vs dense neural networks on image classification
- Evaluate how depth affects performance and generalization
- Analyze the impact of regularization (dropout, batch normalization, L2)
- Understand trade-offs between accuracy, stability, and computational cost

## Methodology
- Dataset: CIFAR-10 (60,000 images, 10 classes)
- Framework: TensorFlow / Keras
- Models:
  - Dense Neural Networks (2–3 layers)
  - Convolutional Neural Networks (2–3 conv blocks)
- Regularization Techniques:
  - Dropout
  - Batch Normalization
  - L2 Weight Decay
- Training:
  - Adam optimizer
  - Batch size = 64
  - Early stopping based on validation accuracy

## Key Results
- Dense neural networks consistently underperformed
  - Failed to capture spatial structure in images
- CNNs significantly outperformed dense models
  - Learned hierarchical features (edges → textures → shapes)
- Increasing depth improved performance in CNNs, but:
  - Led to overfitting without regularization
- Dropout was the most effective regularization method
- Best performance achieved with:
  - CNN + Dropout + Batch Normalization

## Key Insights
- Architecture matters more than regularization alone
- Dense networks cannot compensate for lack of spatial awareness
- CNNs are inherently better suited for image data
- Moderate regularization improves generalization and stability
- Over-regularization reduces model capacity and performance

## Business Impact
- Model selection should prioritize generalization and reliability, not just accuracy
- Poor architecture choices can lead to unreliable real-world performance
- CNN-based models provide more stable and scalable solutions for computer vision applications

## Tech Stack
- Python
- TensorFlow / Keras
- NumPy / Pandas
- Matplotlib / Seaborn
- Scikit-learn

## Conclusion
This study demonstrates that convolutional architectures are fundamentally superior to dense neural networks for image classification tasks. Proper use of regularization further enhances model reliability, making CNNs the preferred choice for real-world deployment.
