
# Image Classification with Feedforward Neural Networks

This project demonstrates the use of **Artificial Neural Networks (ANNs)** for image classification using two benchmark datasets: **Fashion MNIST** and **CIFAR-10**.  
It highlights the strengths and limitations of feedforward ANNs compared to more advanced architectures like Convolutional Neural Networks (CNNs).

---

## Datasets
- **Fashion MNIST**: 70,000 grayscale images (28x28) across 10 fashion categories.
- **CIFAR-10**: 60,000 color images (32x32) across 10 object categories.

---

## Methodology
1. **Preprocessing**
   - Normalize pixel values to [0,1].
   - Flatten images into 1D vectors (784 features for Fashion MNIST, 3072 for CIFAR-10).
2. **Model Architecture**
   - Input: Flattened image vectors.
   - Hidden Layers: Dense layers with ReLU activation.
   - Output: Dense layer with Softmax activation (10 classes).
3. **Training**
   - Optimizer: Adam
   - Loss: Sparse categorical crossentropy
   - Batch size: 64
   - Epochs: 15–20
   - Validation split: 10%
4. **Evaluation**
   - Accuracy, precision, recall, F1-score
   - Confusion matrix and classification report

---

## Results
- **Fashion MNIST**: ~85–88% accuracy with ANN.
- **CIFAR-10**: ~45–55% accuracy with ANN (shows need for CNNs).
- Visualizations include:
  - Training/validation accuracy and loss curves
  - Confusion matrix heatmaps

---

## Setup Instructions

### Requirements
- Python 3.8+
- TensorFlow 2.x
- NumPy, Matplotlib, Seaborn, scikit-learn
