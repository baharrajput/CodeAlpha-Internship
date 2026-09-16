# CodeAlpha Task 3 – Handwritten Character Recognition

## Overview
This project was completed as part of the **CodeAlpha Machine Learning Internship – Task 3**.

The objective is to recognize handwritten digits, uppercase letters, and lowercase letters from grayscale images using a Convolutional Neural Network (CNN).

## Dataset
**EMNIST ByClass**

The dataset contains **62 character classes**:
- Digits: 0–9
- Uppercase letters: A–Z
- Lowercase letters: a–z

### Dataset Statistics

| Dataset | Samples | Image Size |
|---|---:|---:|
| Training | 697,932 | 28 × 28 |
| Testing | 116,323 | 28 × 28 |
| Total | 814,255 | 28 × 28 |

A 10% stratified validation split was created from the original training set.

## Preprocessing
- Images converted to float32
- Pixel values normalized from 0–255 to 0–1
- Channel dimension added for CNN input
- Label mapping created for all 62 classes
- Stratified validation split created

## CNN Architecture
The final custom CNN consists of:

- Input: 28 × 28 × 1
- Conv2D: 32 filters, 3 × 3
- MaxPooling2D
- Conv2D: 64 filters, 3 × 3
- MaxPooling2D
- Flatten
- Dense: 128 neurons
- Dropout: 0.30
- Softmax output: 62 classes

**Total parameters:** 428,350

## Training
- Optimizer: Adam
- Learning rate: 0.001
- Loss: Sparse Categorical Crossentropy
- Early Stopping
- Model Checkpoint
- ReduceLROnPlateau

## Final Results

| Metric | Result |
|---|---:|
| Test Accuracy | **87.04%** |
| Macro Precision | **79.81%** |
| Macro Recall | **73.93%** |
| Macro F1 Score | **74.18%** |
| Weighted F1 Score | **85.65%** |
| Test Loss | **0.3537** |

## Prediction Interface
A modern **Gradio prediction interface** was developed for the trained CNN.

Users can:
- Upload a handwritten character image
- Automatically preprocess the image
- Predict the character
- View prediction confidence
- View the top-5 predictions

The interface is designed for **single-character recognition**, not complete words or sentences.

## Technologies Used
- Python
- Google Colab
- TensorFlow
- Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Gradio

## Project Structure

```text
Task-3-Handwritten-Character-Recognition/
│
├── Task_3_Handwritten_Character_Recognition.ipynb
├── README.md
└── screenshots/
    ├── prediction-ui.png
    ├── confusion-matrix.png
    └── training-results.png
```

## How to Run
1. Open the notebook in Google Colab.
2. Download/load the EMNIST ByClass dataset.
3. Run the preprocessing cells.
4. Train the CNN model.
5. Evaluate the model on the test set.
6. Launch the Gradio interface.
7. Upload a single handwritten character image.

## Internship
**Program:** CodeAlpha Machine Learning Internship  
**Task:** Task 3 – Handwritten Character Recognition

