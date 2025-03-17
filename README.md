# Emotion-Based Music Recommender

This project is an Emotion-Based Music Recommender system that uses facial and hand landmarks detected through a webcam to infer the user's emotion and recommend music based on that emotion.

## Features

- **Real-time Emotion Detection**: Utilizes Mediapipe's holistic model to detect facial and hand landmarks in real-time.
- **Emotion Classification**: A pre-trained Keras model (`model.h5`) classifies the detected landmarks into a specific emotion.
- **Music Recommendation**: Based on the detected emotion, the application suggests music by searching on YouTube.

## Installation

1. Clone the repository**:

```bash
   git clone https://github.com/Gayathri-Selvaganapathi/emotion_based_music_recommendation.git
   cd emotion_based_music_recommendation
```
2. Install the necessary dependencies:

Ensure you have Python 3.7+ installed, then run:

```bash
pip install -r requirements.txt
```

3. Prepare the model and label files:

    * Place your pre-trained Keras model (model.h5) in the project directory.
    * Place your label file (labels.npy) in the project directory. This file should contain the class names corresponding to the emotions your model can detect.

## Usage
1. Run the Streamlit application:

```bash
streamlit run app.py
```

2. Interact with the application:

    * The application will start the webcam and detect your emotion in real-time.
    * Once the emotion is detected, you can click the "Recommend me songs" button to open YouTube with a search query based on your emotion.
    * The application will search YouTube for songs that match your detected emotion.

## Files
    * app.py: The main script to run the application.
    * model.h5: The pre-trained Keras model for emotion detection.
    * labels.npy: The labels corresponding to the emotions.

## How It Works
1. Emotion Detection: The application uses Mediapipe to process video frames from the webcam. It detects facial landmarks and hand landmarks.

2. Feature Extraction: The detected landmarks are used as features for emotion classification. These features are normalized relative to specific key points on the face and hands.

3. Prediction: The features are passed through a pre-trained Keras model that predicts the user's emotion.

4. Music Recommendation: Based on the predicted emotion, the application suggests music by generating a YouTube search query.







