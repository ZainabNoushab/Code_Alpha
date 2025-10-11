# 🧠 Handwritten Character Recognition using CNN

This project builds a **Convolutional Neural Network (CNN)** to recognize handwritten digits (0–9) from the **MNIST dataset** using **TensorFlow/Keras**.

---

## 🎯 Objective
To classify handwritten digits accurately using deep learning.

---

## 📚 Dataset
**MNIST Dataset**
- 70,000 grayscale images of handwritten digits (0–9)
- Each image is 28×28 pixels
- Split: 60,000 for training, 10,000 for testing

---

## 🧩 Approach

### 🔹 Step 1: Preprocessing
- Normalized pixel values (0–255 → 0–1)
- Reshaped data into 28×28×1 tensors
- One-hot encoded labels for categorical output

### 🔹 Step 2: CNN Architecture
```
Conv2D (32 filters, 3×3, ReLU)
MaxPooling2D (2×2)
Conv2D (64 filters, 3×3, ReLU)
MaxPooling2D (2×2)
Flatten
Dense (128 units, ReLU)
Dropout (0.3)
Dense (10 units, Softmax)
```


### 🔹 Step 3: Training
- Optimizer: **Adam**
- Loss: **Categorical Crossentropy**
- Epochs: **10**
- Batch Size: **64**
- Validation Split: **0.2**

---

## 📈 Results
- ✅ **Test Accuracy:** ~98%  
- 🧠 Model generalizes well on unseen handwritten digits.

---

## 🖼️ Visualization
- Training vs Validation Accuracy over epochs  
- Prediction examples with actual vs predicted labels  

---

## 🧪 Sample Prediction
```python
# Predict a random test image
index = np.random.randint(0, len(X_test))
sample = X_test[index].reshape(1,28,28,1)

pred = np.argmax(model.predict(sample))
actual = np.argmax(y_test[index])
```

## 🚀 Future Improvements

- Add EMNIST dataset (for handwritten letters)

- Deploy using Flask or Streamlit web app

- Integrate handwriting input via drawing pad

## 🧠 Tech Stack

Python

TensorFlow / Keras

NumPy, Matplotlib

## ✨ Acknowledgments

Dataset: MNIST

Inspiration: Deep Learning for Computer Vision

| 💬 “Machines can recognize handwriting — but persistence helps us write our success story.”
