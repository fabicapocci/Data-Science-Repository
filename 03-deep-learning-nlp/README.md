# Fake News Detection with NLP and Neural Networks

## Overview

This project applies Natural Language Processing (NLP) and machine learning techniques to classify news articles using their textual content.

The project compares a traditional Multinomial Naive Bayes classifier with a Multi-Layer Perceptron (MLP) neural network for fake-vs-real news detection. A separate multi-class experiment predicts the subject category of news articles.

## Project Workflow

The analysis includes:

- Exploratory data analysis
- Missing-value handling
- Text preparation
- Article-length and word-frequency analysis
- Count Vectorization
- TF-IDF feature extraction
- Stratified train/test splitting
- Multinomial Naive Bayes classification
- MLP neural network classification
- Multi-class subject classification
- Model evaluation and comparison

## Models

Three classification experiments were performed:

- Multinomial Naive Bayes — Fake vs. Real News
- MLP Neural Network — Fake vs. Real News
- MLP Neural Network — News Subject Classification

## Model Performance

| Model | Accuracy |
|---|---:|
| Multinomial Naive Bayes | 93.9% |
| MLP — Fake vs. Real | 99.1% |
| MLP — Subject Classification | 71.1% |

The MLP achieved the strongest performance on the binary fake-vs-real classification task.

The subject-classification experiment was considerably more challenging because the model had to distinguish among multiple news categories with overlapping vocabulary and different numbers of training examples.

## Key Findings

The results demonstrate that TF-IDF features can effectively represent news text for machine learning. Multinomial Naive Bayes provided a strong and computationally efficient baseline, while the MLP achieved substantially higher performance on the binary classification task.

The project also highlights the importance of preventing target leakage and evaluating classification models using metrics beyond accuracy alone.

Although the binary MLP achieved very high performance on this dataset, the results should not automatically be interpreted as equivalent real-world performance. Dataset-specific vocabulary, writing styles, and source characteristics may contribute to the high classification accuracy.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- WordCloud
- Jupyter Notebook

## Project File

[`fake_news_nlp.ipynb`](./fake_news_nlp.ipynb)

The notebook contains the complete exploratory analysis, text preprocessing, model training, evaluation, and conclusions.
