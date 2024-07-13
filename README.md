# CIFAR10_Analysis
Applying multiple model architecture on CIFAR10 dataset for detailed analysis

# CIFAR-10 Model Analysis

## Overview

We have developed multiple models using Keras' Sequential API to analyze the CIFAR-10 dataset, with varying architectures and hyperparameters to find the optimal configuration for training and validation accuracy.

### Model Setup

- **Activation Functions:**
  - Hidden layers: ReLU (Rectified Linear Unit)
  - Output layer: Sigmoid
- **Epochs:** Trained for 20 epochs
- **Optimizer:** SGD (Stochastic Gradient Descent)
  - Updates parameters using gradients computed on a mini-batch, making it suitable for large datasets.
  - Important hyperparameters include learning rate, momentum, and decay rate, which are adjustable based on model requirements.

### Model Configurations

- **Model 1:** 8 layers
- **Model 2:** 7 layers
- **Model 3:** 9 layers

### Training and Validation Accuracy

We plotted training and validation accuracies for each model for a direct comparison:

- **Model 2** (7 layers) exhibited the highest training and validation accuracies.
- **Model 3** showed competitive training accuracies but lagged in validation accuracy compared to Model 2.
- **Model 1** displayed comparable levels of training and validation accuracies.

### Regularization Comparison

- **Original Model vs. Dropout (0.25) vs. Dropout (0.25) + L2 Regularization (1e-04):**
  - The original model outperformed others over increasing epochs in both training and validation accuracies.
  - At 10 epochs, models with dropout and L2 regularization initially showed higher training accuracy, but this advantage diminished with more epochs.

### Optimizer Analysis

- **RMSProp vs. SGD vs. Adam:**
  - RMSProp significantly outperformed SGD and Adam, achieving better training and validation scores from the outset.
  - Adam outperformed the original SGD model, indicating that RMSProp optimizers facilitate faster and more effective training.

### Dropout and Optimizer Impact

- Comparison between dropout effects and optimizer performance:
  - Training accuracies were similar up to 6 epochs across models; thereafter, the Adam model consistently outperformed the dropout model, except at epoch 6 and 18.

### Conclusions

- Models with **7 layers** were generally superior to those with 8 or 9 layers.
- Use of dropouts initially showed promising results but was eventually outpaced by the original model as epochs increased.
- The **RMSProp optimizer** proved more effective than both Adam and SGD. Additionally, Adam was more effective than the SGD combined with dropout.

This analysis highlights the critical impact of layer architecture, dropout usage, and optimizer choice on the performance of deep learning models trained on the CIFAR-10 dataset.

