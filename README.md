# Active Learning with Different Query Strategies

## Project Overview
This project explores the use of Active Learning with different query strategies to classify data from 3 well-known datasets: Iris and Digits. The project demonstrates several query strategies such as Random Sampling, Uncertainty Sampling (Least Confidence, Margin, and Entropy), and Query By Committee (QBC).
The goal is to enhance the classifier performance by intelligently selecting which data points to label using Active Learning approaches.

## Datasets
The following datasets were used in this project:
1. Iris Dataset: A classic dataset containing 150 samples of iris flowers, with 4 features describing each sample. The dataset is divided into 3 classes.
2. Digits Dataset: A dataset containing 1,797 samples of handwritten digits, with 64 features per sample, representing pixel values. The goal is to classify digits from 0 to 9.
3. BMI Dataset: A dataset with features describing an individual's body measurements, used for BMI classification.
## Methodology
### 1. Dimensionality Reduction (PCA)
Principal Component Analysis (PCA) is applied to reduce the feature space of the datasets (Iris and Digits) to 2 dimensions for visualization and decision boundary plotting purposes.

### 2. Active Learning Query Strategies
We employ the following query strategies to decide which unlabeled samples to request labels for:
1. Random Sampling: Selects random data points for labeling.
2. Uncertainty Sampling:
  * Least Confidence: Selects data points where the classifier is least confident in its predictions.
  * Margin Sampling: Selects data points where the classifier's confidence in the top two classes is closest.
  * Entropy: Selects data points with the highest prediction uncertainty (entropy).
3. Query by Committee: Uses an ensemble of classifiers to select data points with the highest disagreement among the classifiers.

### 3. Classification Model
The classifier used in this project is a RandomForestClassifier, wrapped inside SklearnClassifier to work seamlessly with the active learning strategies.

## Evaluation
For each query strategy, the accuracy and F1 score of the classifier are evaluated over 20 active learning cycles. Performance metrics are plotted over time, showing how each strategy performs as more samples are labeled.

## Results
The results demonstrate the performance of different query strategies for active learning, showing how uncertainty-based methods outperform random sampling in terms of accuracy and F1 scores across multiple iterations.

## Conclusion
This project highlights how Active Learning can be used to efficiently select informative samples, thus reducing the amount of labeled data required while still maintaining high classification performance. By applying different query strategies, the project explores ways to improve the training process by leveraging uncertainty-based sampling.
