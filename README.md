CodeAlpha Machine Learning Internship

Overview

This repository contains my work completed during the CodeAlpha Machine Learning Internship.

It includes two machine learning and deep learning projects covering Speech Emotion Recognition and Handwritten Character Recognition. Both projects were developed and tested using Google Colab and include trained deep learning approaches along with interactive prediction interfaces.

Projects

Task 2 – Emotion Recognition from Speech

This project focuses on recognizing human emotions from speech audio using deep learning.

Dataset: RAVDESS
Classes: 8 emotions
Final Model: Wav2Vec2 XLSR Large (facebook/wav2vec2-large-xlsr-53)
Test Accuracy: 78.75%
F1 Score: 78.73%

The project includes MFCC-based experiments, Wav2Vec2-based modeling, evaluation, and a Gradio interface for uploading audio and predicting emotions.

View Task 2 →

Task 3 – Handwritten Character Recognition

This project focuses on recognizing handwritten digits and letters using a Convolutional Neural Network.

Dataset: EMNIST ByClass
Classes: 62
Final Model: Custom CNN
Test Accuracy: 87.04%
Macro F1 Score: 74.18%

The model recognizes digits (0–9), uppercase letters (A–Z), and lowercase letters (a–z). A Gradio interface was also developed for single handwritten character prediction.

View Task 3 →

Technologies Used

Python

Google Colab

TensorFlow / Keras

PyTorch

Hugging Face Transformers

Wav2Vec2 XLSR

Librosa

NumPy

Pandas

Scikit-learn

Matplotlib

Gradio

Repository Structure

CodeAlpha-Internship/
│
├── README.md
│
├── Task-2-Emotion-Recognition/
│   ├── README.md
│   ├── Task_2_Emotion_Recognition.ipynb
│   └── screenshots/
│
└── Task-3-Handwritten-Character-Recognition/
    ├── README.md
    ├── Task_3_Handwritten_Character_Recognition.ipynb
    └── screenshots/

Key Highlights

Speech emotion classification using pretrained speech representations

Handwritten character classification using CNN

Speaker-independent evaluation for speech recognition

62-class handwritten character recognition

Model evaluation using accuracy, precision, recall, and F1 score

Interactive Gradio prediction interfaces

Complete project notebooks and supporting screenshots

Internship

Program: CodeAlpha Machine Learning Internship
Projects: Task 2 – Emotion Recognition from Speech | Task 3 – Handwritten Character Recognition
