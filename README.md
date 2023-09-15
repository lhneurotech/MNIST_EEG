# EEG to MNIST Prediction using Transformer Architecture

## Project Overview

This project aims to use electroencephalogram (EEG) data to predict MNIST numbers. Identifying the power of transformer-based architectures, this project will strive to adapt it for use with EEG data. The goal is to create a robust model that can efficiently decode EEG patterns to corresponding MNIST digits.

## Dataset
### EEG to MNIST Dataset

For our project we will be using MindBigData's 2023 MNIST-8B dataset that contains 140,000 two second labeled data points. Each data point corresponds to a particular MNIST digit. [Dataset](https://huggingface.co/datasets/DavidVivancos/MindBigData2023_MNIST-8B)

* **EEG data**: Contains raw EEG data captured from 128 channels sampled at 250hz
* **Labesls**: MNIST numbers 0-9 that the subject was both visualizing and listening to

## Model Architecture
### Transformer Based Model

Our model is based on the transformer architecture, which has shown significant success in various machine learning tasks. We adapt the transformer to handle time-series EEG data, extracting patterns and relationships that can predict the MNIST numbers.

### Dependencies
* Python 3.11.x
* Pytorch
* NumPy
* MNE
