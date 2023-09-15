# EEG to MNIST Preprocessing Guide
## Overview
This guide will outline the steps and requirements for preprocessing.py.

## Preprocessing Steps

**1. Loading Data in Chunks**

Given the massive size of this EEG dataset, the CSV file should be read in chunks. It is recommended to use the PyTorch dataloader with an On-the-Fly loading technique to avoid memory issues. Pandas would be a good library for reading the CSV file. 

**2. Data Cleaning**

Ensure the data has no NaN or missing values. If they do exist implement a strategy for handling them (such as interpolation or zero-filling).

**3. Noise Reduction**

Load CSV file into MNE. Implement Notch filtering, Independant Component Analysis, and high and low band pass filtering.

**4. Epoching**

I don't think this step will be too hard the data should already be epoched for us. I have this here in case that isn't the situation.

**5. Baseline Correction**

Apply baseline correction for each epoched data to preserve accuracy.

**6. Convert to Tensor**

This is the final step of the Dataloader. The dataloader '__getitem__' function should then return the EEG signal and the label packaged into a dictionary.

