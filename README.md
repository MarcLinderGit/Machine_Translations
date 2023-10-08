# Neural Machine Translation (NMT) Readme

This repository contains Python code for implementing a Neural Machine Translation (NMT) system. The code is divided into three main files: `preprocessing.py`, `training_model.py`, and `test_function.py`. This README provides an overview of each file and how to use them.

## Files Overview

### 1. `preprocessing.py`

- **Purpose**: This script handles data preprocessing, preparing the input and target sequences for training an NMT model.

- **Key Functions**:
  - Reads and splits the input data from a file (specified in `data_path`).
  - Tokenizes and processes input and target sentences.
  - Builds vocabulary sets for both input and target tokens.
  - Creates one-hot encoded input and target data.
  - Defines dictionaries for token-to-index and index-to-token mappings.
  
- **Usage**: This script should be run first to prepare the data for training the model. Ensure that the data path in `data_path` points to your dataset.

### 2. `training_model.py`

- **Purpose**: This script defines and trains the NMT model using TensorFlow and Keras.

- **Key Functions**:
  - Defines the model architecture, including encoder and decoder layers.
  - Compiles and trains the model using the preprocessed data.
  - Saves the trained model to a file (`training_model.h5`).

- **Usage**: Run this script to create and train the NMT model. Make sure to adjust hyperparameters such as `latent_dim`, `batch_size`, and `epochs` according to your requirements.

### 3. `test_function.py`

- **Purpose**: This script contains functions for testing the trained NMT model on new input sequences.

- **Key Functions**:
  - Loads the trained model from the saved file.
  - Defines functions for decoding input sequences.
  - Demonstrates the model's translation capabilities on a sample dataset.

- **Usage**: After training the model using `training_model.py`, you can use this script to test the model's translation performance on new input sentences.

## Getting Started

1. Ensure you have the required libraries installed, including TensorFlow and Keras.

2. Prepare your translation dataset and specify the data path in `preprocessing.py` (variable `data_path`).

3. Run `preprocessing.py` to preprocess and prepare the data.

4. Run `training_model.py` to create and train the NMT model.

5. Once the model is trained, you can use `test_function.py` to test the model's translation capabilities on new input sentences.

## Note

- Make sure to adjust hyperparameters and the number of training examples as needed, especially if you have a large dataset.

- This code is intended for educational purposes and may require further optimization and customization for specific translation tasks and datasets.

- Ensure you have the necessary hardware resources (GPU) for training the model on larger datasets or with higher dimensions.

- Feel free to explore and modify the code to adapt it to your own NMT tasks and requirements.

