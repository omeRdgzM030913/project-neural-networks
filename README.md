# project-neural-networks
This repository shows a complete Deep Learning pipeline for classifying images from the FashionMNIST database, using PyTorch and two Convolutional Neural Network (CNN) architectures. The project compares the performance of both architectures using accuracy metrics, classification reporting, and confusion matrices.

Project Description

Data Loading and Preparation
The FashionMNIST dataset, containing grayscale images (28x28 pixels) of different clothing and accessories categories, is downloaded and processed.
A split between training, validation and testing is performed to properly assess the model's performance.
Transformations (resizing, normalization) are established and a data augmentation mechanism is created to robusten the model against orientation variations and horizontal flip.

Neural Network Architectures
CNN_1: A simpler approach, with 2 convolutional layers and 1 fully connected layer, intended to offer a good starting point for basic image classification.
CNN_2: A deeper design, with multiple convolutional layers, batch normalization, dropout and tailored hyperparameter settings (learning rate, regularization, etc.) to better deal with variance and improve generalization.

Training and Validation
PyTorch loaders are used to process batches of data (customizable batch_size).
Forward-backward cycles are implemented with the CrossEntropyLoss loss functions and the Adam optimizer (in some cases with a scheduler to reduce the learning rate).
Accuracy and loss metrics are recorded at each epoch, both in training and validation, to ensure clear tracking of convergence.

Evaluation and Comparison
Test set: The final models are applied on unseen data to measure the real effectiveness of the classification.
A classification report (precision, recall, F1-score) and a confusion matrix are presented to diagnose the most difficult classes and observe possible imbalances.
Evolution graphs (accuracy and loss) are analyzed to compare whether an architecture has better performance, faster convergence, or less overfitting.

Results and Observations
Both models offer competitive results in FashionMNIST, with CNN_2 being more sophisticated and robust against validation data.
The use of data augmentation and batch normalization shows notable improvements in generalization capacity.
A step-by-step guide on how to adjust hyperparameters to optimize training is provided.

My Qualities in Data Science

Dataset Management: Downloading and preprocessing (transformations, stratified divisions, data augmentation).
Deep Learning Model Design: Configuration of convolutional layers, regularization (dropout, batch normalization), loss functions and optimizers.
Experimentation and Fine-Tuning: Adjustment of hyperparameters (learning rate, epochs, batch size), scheduler for LR decay.
Visualization and Analysis of Results: Confusion Matrix, Classification Report, graphs of loss and accuracy evolution.
Best Practices in PyTorch: Use of DataLoader, separation of training/validation/testing, device control (CPU/GPU/MPS) and code modularization.
