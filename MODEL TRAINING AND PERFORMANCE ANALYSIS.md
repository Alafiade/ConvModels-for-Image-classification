# Project Overview
This project focuses on training a deep learning model to classify images while analyzing 
its performance and ensuring minimal overfitting. This project demonstrates how to optimize  
training for generalization on unseen data by leveralging neural network architectures and 
applying effective regularization techniques.

# Goals of the Project
1. To train and evaluate a CNN on a multi-class image classification task.
2. To reduce overfitting by applying regularization techniques like L2 weight decay and dropout.
3. To analyze and visualize the training and validation metrics.

# Dataset Description
The dataset used in this project conists of three distinct image classes:
. Benign
. Malignant
. Normal
Each class folder contains labeled images representing specific categories relevant to the problem statement.
The dataset is pre-processed to resize the images and normalize their pixel values for compatability with the 
CNN.
. Training Set: Images ussed for model training
. Validation Set: Images used during training to validate performance and detect overfitting.

# Model Description
The model used in this project is a pretrained ResNet101, a robust Convolutional Neural Network known for its residual learning capabilities,
which prevent vanishing gradients during backpropagation. 
Transfer learning was utilized by fine-tuning the pretrained model on the given dataset, modifying its fully connected (FC) layer to output predictions for three classes.

# Training Process
.Epochs: 20
.Optimizer: SGD optimizer with a learning rate of 1e-4.
.Loss Function: CrossEntropyLoss, suitable for multi-class classification.
.Regularization:
 L2 Weight Decay: A regularization parameter of 0.1 was used to reduce overfitting.
 Dropout: Applied to the FC layers to prevent co-adaptation of neurons.

# Performance Metrics
Training Logs:
*Accuracy:
 Training accuracy improved steadily, reaching ~74.7% by the final epoch.
 Validation accuracy showed consistent improvement, peaking at ~73.9%.
*Loss:
 Training loss decreased consistently, indicating effective learning.
 Validation loss stabilized and remained close to training loss, indicating no significant overfitting.
*Graphs:
. Training vs. Validation Accuracy:
  Showed consistent alignment between training and validation curves, indicating strong generalization.
. Training vs. Validation Loss:
  Loss curves decreased steadily and remained close, indicating minimal overfitting.
