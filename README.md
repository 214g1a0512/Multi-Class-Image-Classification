# Multi-Class-Image-Classification
Multi-class image classification on the CIFAR-10 dataset using a Convolutional Neural Network (CNN) model built with Keras. Here's a breakdown of each section:

1. Data Processing
Loading the Dataset: CIFAR-10 is loaded and divided into training and testing sets.
Visualization: A random training image is displayed with its label.
Label Encoding: Labels are one-hot encoded for multi-class classification.
Normalization: Pixel values are scaled to the range [0, 1] for faster convergence.
Data Saving: The test data (x_test and y_test_one_hot) is saved in a Data directory for later use.
2. Building and Training the CNN
Model Structure: A CNN model is created with:
Two sets of Conv2D, activation, and pooling layers with dropout, which help in extracting spatial features and reducing overfitting.
A Flatten layer to convert feature maps to a 1D vector.
A dense layer of 512 units followed by dropout.
An output layer with softmax activation to classify images into 10 categories.
Compilation: The model is compiled using categorical cross-entropy as the loss function and the Adam optimizer.
Training: The model is trained on the training set with 20 epochs, and 20% of the training data is used for validation.
3. Model Evaluation
Training/Validation Performance: Accuracy and loss graphs for both training and validation data are plotted for each epoch.
Testing Performance: The model’s accuracy on the test set is printed.
4. Prediction and Evaluation on Test Set
Model Loading: The saved model and test data are loaded.
Prediction: The model's predictions on the test data are compared with actual labels.
Performance Metrics: Correct and incorrect predictions are counted, and a sample incorrect prediction is visualized.
Classification Report: A detailed classification report is generated, showing metrics like precision, recall, and F1-score for each category in CIFAR-10.

The code provides a comprehensive setup for training, evaluating, and interpreting a CNN on a multi-class image classification task using CIFAR-10.
