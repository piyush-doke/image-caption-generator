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

A brief description of the notebook is provided below.

NOTE: For both training and predicting, cells are to be run sequentially in a top-to-bottom order.

### 1. Training the Model

Implemented in [image_caption_generator.ipynb](/image_caption_generator.ipynb).

Cell Title | Cell Description
:---: | ---
Import Modules | Imports all the required modules.
Settings | Sets the following parameters: seeds, split fraction, iterations of Bayesian optimization, and epochs for training the CNNs.
Functions | Defines the following entities: CNN structures, image augmentations, Bayesian optimization algorithm, and evaluation metrics.
Create Train/Test Sets | Splits the dataset into train and test sets. The train set undergoes image augmentation and test set remains unaugmented. Hold-out validation is used here.
Preview Samples | Displays samples from the train set.
Compare Structures | Trains 6 different CNN structures, each tuned using Bayesian optimization. Compares their accuracy, sensitivity, specificity, and precision.
