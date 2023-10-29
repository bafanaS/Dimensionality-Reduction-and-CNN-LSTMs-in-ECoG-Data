
# Brain Activity Classification for Motor Rehabilitation

This repository is dedicated to research on optimizing motor imagery classification algorithms for Brain-Computer Interfaces (BCIs). The aim is to substantially enhance rehabilitation outcomes for individuals with motor impairments, often caused by neurological incidents such as strokes or traumatic brain injuries.

## Overview

The work leverages data from the [Miller 2010 motor imagery dataset](https://osf.io/ksqv8/) and focuses on:

- Exploratory analysis of the electrocorticographic (ECoG) data
- Dimensionality reduction techniques
- Implementation of supervised deep learning models like CNNs and LSTMs
- Transfer learning strategies

This research critically evaluates the utility of unsupervised techniques like Uniform Manifold Approximation and Projection (UMAP) in conjunction with K-Nearest Neighbors (KNN), alongside traditional supervised methods. The aim is to minimize the need for extensive data labeling and computational resources, while maintaining or improving classification accuracy.

## Notebooks

### Exploratory Analysis

- Data cleaning, reformatting, and statistical analysis
- Comparison between real and imaginary movements using bootstrapping, Fourier analysis, PSD, coherence, and ERB

### Dimensionality Reduction - 2 Classes

- Dimensionality reduction on real vs imaginary movements for individual participants
- Algorithms tested: PCA, t-SNE, UMAP

### Dimensionality Reduction - 4 Classes

- Extends dimensionality reduction to include 4 classes: real hand, real tongue, imaginary hand, imaginary tongue

### CNN/LSTM Classifiers

- Develops CNN and LSTM models to classify real vs imaginary movements
- Utilizes KerasTuner for hyperparameter tuning

### Transfer Learning

- Applies transfer learning techniques to adapt the models for new participants
- Freezes initial layers and retrains later dense layers for fine-tuning

## Models

### Best Performing Models

- **CNN**: Best for real vs imaginary movement classification
- **CNN-LSTM**: Optimal for 2-class classification involving movement type and modality

These models serve as a robust baseline for future research and can be adapted to individualized needs.

## Findings

Participants who scored high on KNN following UMAP dimensionality reduction also exhibited high accuracy rates in supervised deep learning models. This highlights the efficacy of dimensionality reduction as a preprocessing step, reducing the need for extensive labeling and supervised learning.

## Implications

The work has broad implications, extending from targeted therapies for motor dysfunction to addressing regulatory, safety, and reliability concerns in BCIs.

## Usage

The repository provides complete code examples for:

- Data loading and preprocessing
- Dimensionality reduction
- Building, training, and evaluating models
- Hyperparameter tuning
- Transfer learning

For any questions or issues, please open a GitHub issue.