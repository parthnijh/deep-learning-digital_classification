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

## Learnings
1. Loss tells us how far off the predictions were from the actual labels
2. Optimizer acts like the brain and aims on imporiving the predictions ,"adam" here
3. A neuron is a mathematical function that takes inputs assigns them weights ,adds a bias and finally passes them through an activation function
4. keras.sequential adds layers sequentially which contain input hidden and output layers ,input layer essentially flatttens the 2d arrays and output layer gives output in desired number of neurons
   



## ⚙ Training Setup
We compile the model with:

```python
model.compile(
    optimizer='adam',  # How the model updates weights
    loss='sparse_categorical_crossentropy',  # Measures prediction error
    metrics=['accuracy']  # Tracks model performance
)



