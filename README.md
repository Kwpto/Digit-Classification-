# Handwritten Digit Classification using MNIST
This project implements an end-to-end handwritten digit classification pipeline using the MNIST dataset.
A neural network is trained to recognize digits (0–9), and the trained model is used to predict the digit
from a user-provided image.


The model is a fully connected neural network consisting of:
- Flatten layer to convert 28×28 images into a 784-dimensional vector
- Dense layer with 128 neurons and ReLU activation
- Dropout layer to reduce overfitting
- Output Dense layer with 10 neurons and Softmax activation


Loss Function: Sparse Categorical Crossentropy  
Optimizer: Adam  
Evaluation Metric: Accuracy


The model is trained on the MNIST training dataset and evaluated on the test dataset.
After training, the model achieves high accuracy on handwritten digit classification.

The project includes a prediction pipeline that allows users to input an external image of a handwritten digit.
The image preprocessing steps are:

1. Load the image in grayscale
2. Invert colors to match MNIST format
3. Apply thresholding to remove noise
4. Crop the digit using bounding box detection
5. Resize the image to 28×28 pixels
6. Normalize pixel values to range [0, 1]
7. Feed the image into the trained model
8. Output the predicted digit as text

The model was also tested on handwritten digit images created using MS Paint.
After preprocessing, the model correctly recognized the digit from the external image input.