# Image Caption Generator

NOTE: Created in Python 3


## Description

An LSTM network conditioned over Inception v3 for predicting image captions

The images below 
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
Load Image Embeddings | Loads image dataset into memory.
Load Image Embeddings | Loads caption dataset into memory.
Show Training Example | Displays samples from the train set.
Prepare Data for Training and Prediction | Preprocesses data for training and prediction. Also defines ultility functions required for batch training.
Defining Model Architecture for Training | Defines the decoder achictecture of the model required for training and making preditions. This consisting of an Inceptionv3 to  LSTM bridge module and a network of LSTM cells.
Load Pre-Trained Weights | Loads any pre-trained weights of the decoder achitecture. NOTE: should only be used if training is to be resumed.
Training Loop | Trains the model.
