# Real-Time-Emotion-Detection
😊 Real-Time Emotion Detection Using CNN
📌 Overview

This project presents a Real-Time Facial Emotion Detection System built using Convolutional Neural Networks (CNNs). The system identifies human emotions from facial expressions captured via a webcam and classifies them into seven categories:

😠 Angry
🤢 Disgust
😨 Fear
😄 Happy
😢 Sad
😲 Surprise
😐 Neutral

The model is trained on the FER-2013 dataset and integrated with OpenCV for real-time inference, enabling applications in human-computer interaction, mental health monitoring, surveillance, and customer experience systems.

🧠 Features
🎥 Real-Time Emotion Detection using webcam.
🧠 Deep CNN Architecture for accurate emotion classification.
📊 Trained on FER-2013 Dataset containing 35,887 facial images.
🖼️ Face Detection using Haar Cascade classifiers.
⚡ Fast and Robust Predictions under varied lighting conditions.
🔄 Scalable Design for integration with advanced architectures like ResNet or EfficientNet.
🏗️ System Architecture
1. Dataset
Name: FER-2013
Image Size: 48 × 48 pixels (grayscale)
Total Images: 35,887
Emotion Classes: 7
Source: Kaggle Facial Expression Recognition Challenge.
2. Data Preprocessing
Normalization of pixel values.
One-hot encoding of emotion labels.
Optional data augmentation to improve generalization.
3. CNN Model Architecture
Layer Type	Configuration
Input	48×48×1 Grayscale Image
Conv2D	64 filters, 3×3, ReLU
MaxPooling	2×2
Conv2D	128 filters, 3×3, ReLU
MaxPooling	2×2
Conv2D	256 filters, 3×3, ReLU
MaxPooling	2×2
Flatten	—
Dense	256 units, ReLU
Dropout	0.5
Dense	128 units, ReLU
Output	7 units, Softmax
4. Training Details
Loss Function: Categorical Crossentropy
Optimizer: Adam (learning rate = 0.001)
Evaluation Metric: Accuracy
5. Real-Time Inference
Face Detection: Haar Cascade (Viola–Jones algorithm).
ROI Processing: Detected faces are resized to 48×48 pixels.
Prediction: The trained CNN model outputs the corresponding emotion label in real time.
