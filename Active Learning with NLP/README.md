# Sentiment Analysis with Active Learning

## Project Overview
This project explores sentiment analysis using a Convolutional Neural Network (CNN) combined with active learning techniques. The goal is to classify tweets into positive or negative sentiments while leveraging active learning to iteratively improve the model's performance. The active learning strategies evaluated include uncertainty sampling, margin sampling, entropy sampling, and random sampling.

## Dataset
The dataset used in this project is the Sentiment140 dataset. It contains 1.6 million tweets, each labeled with a sentiment: 0 for negative and 1 for positive.

## Methodology
### Data Preprocessing
* Text Cleaning: Tweets are cleaned by removing URLs, HTML tags, punctuation, numbers, and stop words.
* Tokenization: Text is converted into sequences of integers using TensorFlow's Tokenizer.
* Padding: Sequences are padded to a fixed length to ensure uniform input size for the model.

### Model Architecture 
The model architecture includes an embedding layer for word vector representation, two 1D convolutional layers for feature extraction, and a global max pooling layer. It also features fully connected dense layers with dropout for regularization and concludes with a single neuron output layer with a sigmoid activation function for binary classification.

### Active Learning
The active learning strategies evaluated include uncertainty sampling, margin sampling, entropy sampling, and random sampling.

#### Active Learning Cycle:
1. Start with an initial training set.
2. Iteratively query the learner to select the most informative samples.
3. Teach the model with the queried samples.
4. Evaluate and update the model's performance.

## Results
The model was evaluated across several active learning iterations. The accuracy improved over time as the model was exposed to more informative samples. 

## Conclusion
This project demonstrates the effectiveness of active learning strategies in enhancing sentiment analysis models. By integrating active learning with a CNN model, we achieve improved classification performance on the sentiment analysis task.

