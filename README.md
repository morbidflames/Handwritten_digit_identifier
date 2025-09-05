# 📘 Handwritten Digit Identifier  

This project builds and trains **neural network models** to classify handwritten digits (0–9) from the **MNIST dataset**. Two architectures are implemented:  
1. A **Simple Sequential model** (basic feedforward network).  
2. A **Complex Multi-path model** (branching architecture with multiple hidden paths).  

---

## 📂 Dataset  
- **MNIST dataset** (60,000 training images + 10,000 test images).  
- Each image is grayscale, **28×28 pixels**.  
- Labels: digits from **0 to 9**.  

---

## 🏗️ Model Architectures  

### 🔹 1. Simple Sequential Model  
- It takes a 28×28 image and flattens it into a 1D vector.  
- Passes the data through a small hidden layer with 5 neurons (ReLU activation).  
- Finally, it uses a softmax output layer with 10 neurons to classify the image into one of the digits (0–9).  

---

### 🔹 2. Complex Multi-path Model 
- The input image is flattened into a vector.  
- The network then splits into two separate paths:  
  - Path A learns features with two hidden layers (128 → 64 neurons).  
  - Path B learns features with a single larger hidden layer (256 neurons).  
- The results of both paths are merged together.  
- A softmax output layer with 10 neurons then classifies the digit (0–9)  

---

## 📊 Results  
- Both models achieve high accuracy on MNIST.  
- **Simple model**: Easier to train, less accurate.  
- **Complex model**: Captures richer features, usually achieves better accuracy.  

---

## 🚀 How to Run  

1. Clone the repository:  
```bash
git clone https://github.com/your-username/handwritten-digit-identifier.git
cd handwritten-digit-identifier
```

2. Install dependencies:  
```bash
pip install tensorflow matplotlib numpy
```

3. Run the notebook:  
```bash
jupyter notebook Handwritten_digit_identifier.ipynb
```

---
