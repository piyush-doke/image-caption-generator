# Image Caption Generator

NOTE: Created in Python 3


## Description

An LSTM network conditioned over Inception v3 for predicting image captions.

The images below show some captions our model has predicted.
<img src="/sample_images/cmb.png" width="400"> | <img src="/sample_images/non_cmb.png" width="400">
:---: | :---:
CMB Samples | Non-CMB Samples


## Frameworks/Tools

- [TensorFlow 1](https://www.tensorflow.org/api_docs/python/tf/compat/v1)


## Usage

NOTE: For both training and predicting, cells are to be run sequentially in a top-to-bottom order.

### 1. Training the Model

Implemented in [image_caption_generator.ipynb](/image_caption_generator.ipynb).

Cell Title | Cell Description
:---: | ---
Mount Drive | Mounts Google Drive to Google Colab. NOTE: Should only be used if working on Google Colab.
Import Libraries | Imports all the required modules.
Download Train and Validation Data | Downloads training and validation data. NOTE: Should only be used if data is not already downloaded.
Load Image Embeddings | Loads the image dataset into memory.
Load Image Embeddings | Loads the caption dataset into memory.
Show Training Example | Displays sample images and their captions from the training set.
Prepare Data for Training and Prediction | Preprocesses data for training and prediction. Also defines ultility functions required for batch training.
Defining Model Architecture for Training | Defines the decoder achictecture of the model required for training and making preditions.
Load Pre-Trained Weights | Loads any pre-trained weights for the decoder architecture. NOTE: Should only be used if training is to be resumed.
Training Loop | Trains the model. Saves learned weights after every epoch and also when the model is done training.

### 2. Training the Model

Implemented in [image_caption_generator.ipynb](/image_caption_generator.ipynb).

Cell Title | Cell Description
:---: | ---
Mount Drive | Mounts Google Drive to Google Colab. NOTE: Should only be used if working on Google Colab.
Import Libraries | Imports all the required modules.
Download Train and Validation Data | Downloads training and validation data. NOTE: Should only be used if data is not already downloaded.
Load Image Embeddings | Loads the image dataset into memory.
Load Image Embeddings | Loads the caption dataset into memory.
Show Training Example | Displays sample images and their captions from the training set.
Prepare Data for Training and Prediction | Preprocesses data for training and prediction. Also defines ultility functions required for batch training.
Define Decoder | Defines the decoder achictecture required for training and making preditions.
Load Pre-Trained Weights | Loads pre-trained weights for the decoder architecture.
Define Encoder | Defines the encoder achictecture required for making preditions.
Prediction Loop | Defines the prediction function
Make Prediction (from validation set) | Applies the model on vaidation data to make predictions.
