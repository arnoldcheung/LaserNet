# LaserNet
A model utlising Facebook AI Research's LASER embeddings for translation quality estimation. Built using PyTorch.

## Archituecture
* Feed forward neural network regressor taking the concatenated English and German LASER embeddings (1024 dimensions each) as input.

## Prerequisites
    pip install laserembeddings
    !python -m laserembeddings download-models    
    pip install torch
    pip install tqdm
* The notebook usee tqdm_notebook for loading bars, recommended to use jupyter notebook or colab to run

## Running Tests
The notebook contain nine sections, run from the beginning for full test:

* Environment Set Up
    * Imports libraries, creates necessary directories, fix random seed and checks GPU
    
* Importing Data
    * Downloads training, validation, and test data.
    
* Laser (testing)
    * Demonstrates the use of laser embeddings
    
* Preparing Data
    * Defines dataloader for training, containing text preprocessing and embedding extraction

* Neural Network
    * Defines the neural network architecture
    
* Training and Evaluation
    * The main training and evaluation loop

* Grid search
    * Implements parameter search over batch size, learning rate and weight decay
    
* Final Evaluation
    * Loads the model, and write predictions to an output file
    
* Results
    * No code, some example results from training
