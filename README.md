# EmotionDetectionCNN

Real-time facial emotion detection using a Convolutional Neural Network. The model can detect 7 emotional states: Angry, Disgust, Fear, Happy, Neutral, Sad, and Surprise.

## Features

* Real-time emotion detection through webcam
  
* Pre-trained model on multiple datasets (FER, CK+, and RAF-DB)
  
* Support for 7 different emotion classes

## Installation

Clone this repository:
```bash
git clone https://github.com/yourusername/EmotionDetectionCNN.git
cd EmotionDetectionCNN
```

Install dependencies:

```bash
pip install tensorflow opencv-python keras numpy
```

Make sure you have the model file and haarcascade file in the correct location:

* haarcascade_frontalface_default.xml (included in repo)

* best_model_after_training_07912.keras (included in repo)



## Usage

Run the application using Python:
```bash
python main.py
```

* The webcam will activate and begin detecting faces and emotions
  
* A label will appear above any detected face showing the predicted emotion
  
* Press 'q' to quit the application

## How the Model Works

### Data Sources

The CNN model was trained on three popular facial expression datasets:

* FER Dataset
  
* CK+ Dataset (Extended Cohn-Kanade)
  
* RAF-DB Dataset (Real-world Affective Faces)


### Model Architecture

The model uses a CNN architecture with:

* 3 convolutional layers with batch normalization and max pooling
  
* 2 fully connected layers with dropout for regularization
  
* Output layer with 7 emotion classes

### Training Process

* Hyperparameter optimization using Keras Tuner
  
* Data augmentation (rotation, shifts, flips) to improve generalization
  
* Fine-tuning with early stopping and learning rate reduction

### Behind the Scenes

The application:

* Captures video from your webcam
  
* Converts frames to grayscale
  
* Detects faces using OpenCV's Haar Cascade classifier
  
* Processes each face (resize to 48x48 pixels, normalize)
  
* Runs the processed face image through the trained CNN model
  
* Displays the predicted emotion label above each detected face

### Further Development

For more details on the model development process, see the facial-recognition.ipynb notebook.
