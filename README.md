# Sentence-ordering-with-RNN-Encoder-Decoder
Sentence Ordering with RNN Encoder-Decoder


This project implements a sequence-to-sequence model using an RNN encoder-decoder architecture to solve the sentence ordering task. The model learns to arrange shuffled sentences into their correct sequential order.

## Overview

While Transformers are currently the state-of-the-art for sequence-to-sequence tasks, this project intentionally uses an RNN encoder-decoder architecture for educational purposes, providing insights into how these fundamental architectures work.

## Features

- LSTM-based encoder-decoder architecture
- Custom data generation and preprocessing pipeline
- Special token handling (`<start>`, `<end>`, `<comma>`)
- Inference pipeline for model testing
- Approximately 10M trainable parameters

## Technical Details

### Dependencies
- TensorFlow
- Keras
- NumPy
- Datasets (Hugging Face)
- Matplotlib

### Dataset
The project uses the `generics_kb` dataset from Hugging Face, with the following preprocessing steps:
- Filters sentences longer than 8 words
- Adds special tokens
- Implements custom tokenization

### Model Architecture
- Embedding dimension: 128
- LSTM units: 256
- Dropout rate: 0.3
- Vocabulary size: 10,000
- Optimizer: Adam
- Loss: Sparse Categorical Cross Entropy

## Training

The model is trained for 10 epochs with the following specifications:
- Batch size: 32
- Training samples: 220,000
- Test samples: 21,216


## Model Performance

The model demonstrates the ability to:
- Understand sentence structure
- Correctly position nouns and verbs
- Maintain grammatical coherence in outputs

While not achieving state-of-the-art performance (which belongs to Transformer architectures), it provides a solid baseline and educational example of sequence-to-sequence modeling.

## Future Work

- Implementation of the same task using Transformers for performance comparison
- Hyperparameter optimization
- Exploration of different RNN architectures

## Author

Ali Akbar Halvaei  
Email: ali.akbarhalvaei@studio.unibo.it
