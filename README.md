# MNIST-CNN-Classifier
An introductory deep learning project focused on image classification. This repository implements a multi-layer Convolutional Neural Network (CNN) to classify the 10 handwritten digits (0-9) from the MNIST dataset. The model architecture features Conv2D and MaxPooling layers, successfully achieving a test accuracy of 99.18%
## 💡 Project Goal

The primary objectives of this project are:

* **Demonstrate CNN Power:** To showcase how the CNN architecture outperforms a simple neural network by utilizing superior feature extraction capabilities on image data.
* **TensorFlow/Keras Foundations:** To establish a complete deep learning pipeline (data pre-processing, model building, training, and evaluation) using the Keras API.
* **Baseline Comparison:** To compare the final CNN model's accuracy against a simpler feedforward network baseline.

---

## 🧱 Model Architecture

The CNN model is designed for efficiency and high accuracy. 

![CNN Model Accuracy Plot]("C:\Users\Asus\OneDrive\Pictures\Accuracy.png")
 The core architecture is as follows:

| Layer | Output Shape | Parameters | Description |
| :--- | :--- | :--- | :--- |
| **Conv2D (32 Filters)** | (26, 26, 32) | 320 | Initial feature extraction using a 3x3 kernel. |
| **MaxPooling2D** | (13, 13, 32) | 0 | Reduces dimensions by 2x2 to decrease complexity. |
| **Conv2D (64 Filters)** | (11, 11, 64) | 18,496 | Learns more complex patterns. |
| **MaxPooling2D** | (5, 5, 64) | 0 | Further reduces dimensions. |
| **Dropout (0.25)** | | | Helps prevent overfitting. |
| **Flatten** | (1600) | 0 | Converts the data into a 1D vector for classification. |
| **Dense (128)** | (128) | 204,928 | Hidden layer. |
| **Dense (10)** | (10) | 1,290 | Final output layer (Softmax Activation). |

**Total Parameters:** $\approx 225,000$

---

## Results

After training, the model achieved the following key metrics:

| Metric | Baseline Model (Notebook 1) | CNN Model (Notebook 2) |
| :--- | :--- | :--- |
| **Test Accuracy** | ~97% (Approx) | **99.18%** |
| **Test Loss** | ~0.08 | **0.0330** |

---

## 🛠️ Requirements and Setup

This project requires Python and specific deep learning and data manipulation libraries.

### Prerequisites

* Python 3.x
* Jupyter Notebook or Google Colab

### Install Libraries

You can install the necessary libraries using the following command:

```bash
pip install tensorflow matplotlib numpy
