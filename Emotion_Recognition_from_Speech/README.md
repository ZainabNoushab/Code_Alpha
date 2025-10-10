# 🎙️ Emotion Recognition from Speech using Deep Learning
## 📘 Overview

This project aims to recognize human emotions from speech audio using deep learning and speech signal processing techniques.
By analyzing the tone, pitch, and rhythm of speech, the model classifies emotions such as happy, sad, angry, and fearful from the RAVDESS dataset.

## 🎯 Objective

Develop a model that can automatically detect emotions from voice recordings using audio feature extraction and neural network models.

## 🧠 Key Steps
### 1️⃣ Dataset

*Dataset Used:* RAVDESS – Ryerson Audio-Visual Database of Emotional Speech and Song

The dataset contains emotional speech recordings by professional actors, labeled with 8 emotion classes:
neutral, calm, happy, sad, angry, fearful, disgust, surprised

### 2️⃣ Feature Extraction

Each .wav audio file is processed using Librosa to extract acoustic features:

*MFCCs (Mel-Frequency Cepstral Coefficients)* – represent tone and timbre

*(Optional Enhancements):* Chroma, Mel Spectrogram, Spectral Contrast, Tonnetz

### 3️⃣ Model Architecture

Implemented a deep learning classifier using TensorFlow/Keras.

Two common approaches tested:

LSTM / GRU model for temporal sequence modeling

1D CNN model for spatial feature learning

### 4️⃣ Training

*Split dataset:* 80% training / 20% testing

*Optimizer:* Adam

*Loss:* categorical_crossentropy

*Metrics:* accuracy

### 5️⃣ Evaluation

Performance evaluated using accuracy, confusion matrix, and classification report.

### 6️⃣ Predicting New Audio

You can test your own .wav files:
```
file = '/content/sample_audio.wav'
features = extract_features(file).reshape(1, -1)
pred = model.predict(features)
emotion = le.inverse_transform([np.argmax(pred)])[0]
print("Predicted Emotion:", emotion)
```

## 📈 Results

The model achieved around 85–90% accuracy (depending on model and features).
Commonly confused pairs: happy ↔ fearful, calm ↔ neutral.

## 🧰 Tools & Libraries

Python

Librosa – Audio signal processing

NumPy / Pandas / Matplotlib / Seaborn – Data handling and visualization

TensorFlow / Keras – Deep learning

Scikit-learn – Data preprocessing and evaluation

## 🚀 Future Improvements

Add chroma, contrast, and tonnetz features for richer sound representation

Experiment with CNN-LSTM hybrid architectures

Integrate real-time emotion prediction from microphone input

Build a web dashboard (Streamlit / Flask) for live demos
