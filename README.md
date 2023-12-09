# Sign Language to Text Conversion Using LSTM

## Overview

This project utilizes computer vision techniques and LSTM models to convert sign language gestures into text in real-time. It employs TensorFlow and MediaPipe Holistics for gesture recognition and sequence prediction.

## Features

- Real-time sign language recognition
- LSTM model for sequence prediction
- Custom dataset creation using video capture
- Integration with TensorFlow and MediaPipe Holistics
- Support for multiple sign language gestures/actions

## Requirements

- Python 3.9
- TensorFlow
- MediaPipe Holistics

## Installation

 Clone the repository:
 ```bash
    git clone https://github.com/abmath113/SignLanguageTranslator.git
 ```

## Dataset

The dataset used in this project was created by capturing 30 videos for each sign language action at 30 frames per second. The dataset contains a variety of gestures, ensuring robustness in recognition.

## Training

To train the LSTM model on the dataset:

### Data Preparation:
1. Load and preprocess the dataset.
2. Split the dataset into training, validation, and test sets in 95/5 ratio
   
### Model Initialization:
1. Define LSTM Architecture
2. Compile the model with Adam optimizer and categorical cross-entropy loss.
### Training Loop:
1. Loop for a total of 2000 epochs:
2. Forward pass: Input training data through the model.
3. Calculate the loss using categorical cross-entropy.
   Backpropagate the gradients.
4. Update the model's weights using the Adam optimizer.
### Validation:
Periodically, or after each epoch, evaluate the model on the validation set:
Forward pass: Input validation data through the trained model.
Calculate validation loss and other metrics to assess performance.
### Test:
After completing the 2000 epochs, evaluate the final model on the test set:
Input test data through the trained model.
Calculate test set loss and other relevant metrics.

## Results

The model achieved an accuracy of 92% on the validation set and demonstrated real-time conversion of sign language gestures into accurate text with minimal latency.

# Future Improvements:

1. Implementing a more extensive dataset for better generalization
2. Enhancing the LSTM architecture for improved accuracy
3. Developing a user-friendly interface for easier interaction
