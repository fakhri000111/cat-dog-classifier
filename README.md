# Cats vs Dogs Classification using CNN

A deep learning project that classifies images of cats and dogs using a Convolutional Neural Network (CNN) built with TensorFlow and Keras.

---

## Overview

This project implements a CNN model for **binary image classification**. The model learns visual features from images and predicts whether the input image is a **cat** or a **dog**.

- Framework: TensorFlow / Keras  
- Task: Binary Classification  
- Input Size: 128 × 128 × 3  
- Output: Probability (Sigmoid)

---

## Model Architecture

The model follows a structured deep CNN pipeline:
Conv2D(32) → BatchNorm → MaxPool
Conv2D(64) → BatchNorm → MaxPool
Conv2D(128) → BatchNorm → MaxPool
Flatten → Dense(128) → Dropout → Output

### Key Features:
- **Batch Normalization** → stabilizes training
- **Dropout (0.6)** → reduces overfitting
- **L2 Regularization** → improves generalization
- **He Initialization** → optimized for ReLU layers

---

## Hyperparameters

| Parameter        | Value        |
|-----------------|-------------|
| Image Size       | 128 × 128   |
| Optimizer        | Adam        |
| Learning Rate    | 0.0008      |
| Loss Function    | Binary Crossentropy |
| Dropout          | 0.6         |
| Regularization   | L2 (0.001)  |

---

##  Callbacks

### Early Stopping
Stops training when validation loss stops improving.
## 📊 Results

The model was trained for 20 epochs with early stopping applied.

### Final Training Metrics

- **Training Accuracy:** 90.64%
- **Training Loss:** 0.3814

### Validation Metrics

- **Validation Accuracy:** 84.23%
- **Validation Loss:** 0.6581

---

### Training Insights

- The model achieved strong training accuracy (~90%), indicating good learning of features.
- Validation accuracy (~84%) shows decent generalization to unseen data.
- Slight gap between training and validation accuracy suggests **mild overfitting**, which is expected in CNNs.

---

### Observations

- Validation loss is higher than training loss → model is slightly overfitting
- Dropout (0.6) and L2 regularization helped control overfitting
- Performance is stable across epochs (no major fluctuations)

---

### Conclusion

The model performs well for a basic CNN architecture and can be further improved using:

- Data augmentation
- Transfer learning (ResNet / MobileNet)
- Hyperparameter tuning
