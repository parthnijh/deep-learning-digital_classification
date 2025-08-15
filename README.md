# 🖋 Digit Classification with Neural Networks

This project uses a *Neural Network* built with *TensorFlow/Keras* to classify handwritten digits from the [MNIST dataset](http://yann.lecun.com/exdb/mnist/).

---

## 📌 Project Overview
The MNIST dataset contains *70,000 grayscale images* of handwritten digits (0–9), each sized *28×28 pixels*.  
Our goal: Train a model that takes an image of a digit and predicts the correct number.

---

## 🧠 Model Architecture
We use a simple *feedforward neural network*:

1. *Flatten Layer*  
   - Converts the 28×28 pixel image into a 784-element vector.
   - Example:  
     
     28x28 → [pixel1, pixel2, ..., pixel784]
     

2. *Dense Layer (Hidden Layer)*  
   - 100  
   - Activation: *ReLU*  
   
3.  *Output Layer*  
   - 10 neurons (one per digit 0–9)  
   - Activation: *sigmoid* 

---

## ⚙ Training Setup
We compile the model with:

```python
model.compile(
    optimizer='adam',  # How the model updates weights
    loss='sparse_categorical_crossentropy',  # Measures prediction error
    metrics=['accuracy']  # Tracks model performance
)
