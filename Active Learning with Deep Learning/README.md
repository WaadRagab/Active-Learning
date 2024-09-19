# Active-Learning-with-Deep-Learning

## Project Overview
This project explores active learning techniques using TensorFlow and modAL on various datasets, including CIFAR-10 and Fashion MNIST. The focus is on leveraging different query strategies for active learning 
to improve model performance in classifying images. The performance of these strategies is evaluated using accuracy and F1-score metrics.

## Datasets
1. CIFAR-10: A dataset containing 60,000 32x32 color images in 10 classes, with 6,000 images per class.
2. Fashion MNIST: A dataset of 70,000 grayscale images of 10 fashion categories, with 7,000 images per category.
3. Imbalanced Fashion MNIST: A modified version of the Fashion MNIST dataset with imbalanced class distributions to test the robustness of active learning strategies.

## Methodology
### Data Preprocessing
* Normalization: Image data is scaled to have pixel values between 0 and 1.
* One-Hot Encoding: Labels are converted into categorical format suitable for classification.

### Active Learning Query Strategies
The focus is on leveraging different query strategies for active learning, such as uncertainty sampling, margin sampling, entropy sampling, and random sampling.
 ### Model Architecture
Convolutional Neural Network (CNN): Consists of three convolutional layers followed by max-pooling, a flattening layer, and two dense layers. The final layer uses a softmax activation function for classification.

### Model Training and Evaluation
* Training: Models are trained using TensorFlow's Keras API with the Adam optimizer and categorical cross-entropy loss.
* Evaluation: The performance of the model is assessed based on accuracy and F1-score across multiple active learning queries.

## Results
Accuracy: Plots showing the accuracy of the model for different query strategies over successive queries.
F1-score: Plots illustrating the F1-score of the model for different query strategies over successive queries.

## Visualizations
Accuracy and F1-Score Plots: Graphs visualizing the performance of various query strategies across different datasets.

## Conclusion
This project demonstrates the effectiveness of various active learning strategies in improving the performance of deep learning models on image classification tasks. 
By employing uncertainty sampling, margin sampling, entropy sampling, and random sampling, the project provides insights into the most effective approaches for active learning.

