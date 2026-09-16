# CodeAlpha Task 2 – Emotion Recognition from Speech

## Overview
This project was completed as part of the **CodeAlpha Machine Learning Internship – Task 2**.

The objective is to recognize human emotions from speech audio using deep learning techniques. The project explores MFCC-based models and pretrained Wav2Vec2 speech representations.

## Dataset
**RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)**

- 1,440 speech audio files
- 24 actors
- 8 emotion classes
- Audio resampled to 16 kHz
- Speaker-independent train/validation/test split

### Emotion Classes
- Angry
- Calm
- Disgust
- Fearful
- Happy
- Neutral
- Sad
- Surprised

### Data Split

| Split | Actors | Samples |
|---|---|---:|
| Training | 01–16 | 960 |
| Validation | 17–20 | 240 |
| Testing | 21–24 | 240 |

## Approaches
### 1. BiLSTM with MFCC
MFCC features were extracted from audio and classified using a Bidirectional LSTM.

### 2. CNN-LSTM with MFCC
A hybrid CNN-LSTM architecture was tested to learn patterns from MFCC representations.

### 3. Wav2Vec2 Base
A pretrained Wav2Vec2 model was used for speech representation and emotion classification.

### 4. Final Model – Wav2Vec2 XLSR Large
The final selected model uses:

`facebook/wav2vec2-large-xlsr-53`

The model was fine-tuned for the 8-class speech emotion recognition task.

## Final Results

| Metric | Test Result |
|---|---:|
| Accuracy | **78.75%** |
| Precision | **82.55%** |
| Recall | **78.75%** |
| F1 Score | **78.73%** |
| Test Loss | **1.7026** |

## Technologies Used
- Python
- Google Colab
- PyTorch
- Hugging Face Transformers
- Wav2Vec2 XLSR
- Librosa
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Gradio

## Prediction Interface
A modern **Gradio web interface** was developed to test the model.

The interface allows users to:
- Upload an audio file
- Process the audio automatically
- Predict the detected emotion
- Display prediction confidence
- Show top emotion probabilities

## Project Structure

```text
Task-2-Emotion-Recognition/
│
├── Task_2_Emotion_Recognition.ipynb
├── README.md
└── screenshots/
    └── prediction-ui.png
```

## How to Run
1. Open the notebook in Google Colab.
2. Connect/load the RAVDESS dataset.
3. Install the required libraries.
4. Run preprocessing and training cells.
5. Evaluate the model.
6. Launch the Gradio prediction interface.

## Internship
**Program:** CodeAlpha Machine Learning Internship  
**Task:** Task 2 – Emotion Recognition from Speech
