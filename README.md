# Image Caption Generator

NOTE: Created in Python 3


## Description

This is a Long Short-Term Memory (LSTM) network conditioned over Inception v3 for predicting image descriptions. The overall architecture is divided into two modules, namely the encoder and the decoder. The encoder comprises of a pre-trained Inception v3 network, whereas the decoder consists of the actual LSTM text generator. We also consider applying a dense layer connecting the two, this helps transform image embeddings to the RNN's initial state.

The images below show some predictions our model has made.

<br><img src="/sample_predictions/sample_1.png" height="400">

<br><img src="/sample_predictions/sample_2.png" width="400">

<br><img src="/sample_predictions/sample_3.png" width="400">

<br><img src="/sample_predictions/sample_4.png" width="400">


## Frameworks/Tools

- [TensorFlow 1](https://www.tensorflow.org/api_docs/python/tf/compat/v1)


## Usage

NOTE: For both training and making predictions, cells are to be run sequentially in a top-to-bottom order.

### 1. Training

Rather than training over images, we train the decoder directly over image embeddings (produced by Inception v3) for efficiency proposes. And given that we use a pre-trained Inception v3 network, training for the encoder module is skipped.

Implemented in [image_caption_generator.ipynb](/image_caption_generator.ipynb).

Cell Title | Cell Description
:---: | ---
Mount Drive | Mounts Google Drive to Colab. <br>NOTE: Should only be used if working on Colab.
Import Libraries | Imports all the required dependencies.
Download Training and Validation Data | Downloads training and validation data. <br>NOTE: Should only be used if data is not already downloaded.
Load Image Embeddings | Loads the image dataset into memory.
Load Captions | Loads the caption dataset into memory.
Show Training Examples | Displays some sample images and their captions (from training set).
Prepare Data for Training and Making Predictions | Preprocesses data for training and making predictions. Also defines utility functions required for batch training.
Define Decoder | Defines the decoder architecture required for training and making predictions.
Load Pre-Trained Decoder Weights | Loads any pre-trained weights for the decoder architecture. <br>NOTE: Should only be used if training is to be resumed.
Training Loop | Trains the model. Saves learned weights after every epoch and also after the decoder is done training.

### 2. Making Predictions

Implemented in [image_caption_generator.ipynb](/image_caption_generator.ipynb).

Cell Title | Cell Description
:---: | ---
Mount Drive | Mounts Google Drive to Colab. <br>NOTE: Should only be used if working on Colab.
Import Libraries | Imports all the required dependencies.
Download Training and Validation Data | Downloads training and validation data. <br>NOTE: Should only be used if data is not already downloaded.
Load Image Embeddings | Loads the image dataset into memory.
Load Captions | Loads the caption dataset into memory.
Show Training Examples | Displays some sample images and their captions (from training set).
Prepare Data for Training and Making Predictions | Preprocesses data for training and making predictions. Also defines utility functions required for batch training.
Define Decoder | Defines the decoder architecture required for training and making predictions.
Load Pre-Trained Decoder Weights | Loads pre-trained weights for the decoder architecture.
Define Encoder | Defines the encoder architecture required for making predictions.
Prediction Loop | Defines the prediction function.
Make Predictions | Applies the model on images (from validation set) to predict their captions.
