# SVD-Based Text Classification

## Problem Statement
Automatic text classification is essential for retrieving information and organizing tasks in various applications like sentiment analysis, document categorization, and spam detection. However, dealing with high-dimensional text data poses significant computational challenges and can affect classification performance. This project explores the use of Latent Semantic Indexing (LSI), leveraging Singular Value Decomposition (SVD), to reduce dimensionality while preserving semantic relationships in text data for improved classification accuracy.

## Project Architecture
- **Data Collection:** The Reuters Corpus Volume 1 (RCV1) is used, containing news articles with metadata fields like region codes, industry codes, and topic codes.
- **Data Preprocessing:** Text data is cleaned, normalized, and structured through a series of preprocessing steps, including text expansion, tokenization, stop word removal, punctuation removal, and lemmatization.
- **Document Representation:** Text data is converted into a numerical format using Term Document Matrix (TDM) and count vectorization.
- **Dimensionality Reduction:** LSI, based on SVD, is applied to reduce the dimensionality of the TDM, capturing the underlying semantic structure of the document collection.
- **Classification Model:** Multi-Layer Perceptrons (MLPs) are used as the classification model to learn complex non-linear relationships in the data.

## Dataset
The Reuters Corpus Volume 1 (RCV1) is a comprehensive dataset widely used in text classification research. It comprises 806,791 news articles covering diverse topics. Each document is associated with metadata fields, including region codes, industry codes, and topic codes. The dataset supports both single-label and multi-label classification tasks:

Single-Label Classification: In this setup, each document is assigned only one category. This simplifies the classification problem but may not fully capture the complexity of real-world text data.
Multi-Label Classification: Here, each document can belong to multiple categories simultaneously. This setup is more challenging as it requires the model to predict multiple labels for each document.
Subset1 and Subset2 Datasets
To manage computational resources and address class imbalance, two subsets of the dataset are created:

- **Subset1:** This subset is derived from the original dataset by selecting documents that belong to the top 10 most frequent categories( 200 documents from each of the top 10 categories). This reduces the overall size of the dataset while maintaining a representative sample of the most common topics.
- **Subset2:** This subset acknowledges the inherent class imbalance by selecting documents proportionally to their original class distribution. We chose 500 documents each from the top two most populated categories due to their significantly higher document counts (23,935 and 2,674 documents, respectively). The remaining eight categories are included with their original document counts.

## Process

### 1) Data Collection:

The Reuters dataset, consisting of 806,791 XML files, is used.
Single-label and multi-label classifications are considered.
Data subsets (Subset1 and Subset2) are created to address class imbalance and manage computational resources.

### 2) Data Preprocessing:

Text is cleaned and normalized by expanding contractions, converting to lowercase, tokenizing, removing stop words and punctuation, and lemmatizing.
The Term Document Matrix (TDM) is created using count vectorization.
### 3) Dimensionality Reduction:

LSI is applied using SVD to decompose the TDM into three components: U (left singular vectors), Σ (singular values), and V^T (right singular vectors).
The impact of varying the number of latent dimensions (K) on classification performance is explored.
### 4) Classification Model:

Multi-Layer Perceptrons (MLPs) are used for text classification.
Experiments are conducted to understand how varying latent dimensions influence classification performance.
## Results
The study demonstrates that using 100 to 500 latent dimensions significantly improves text classification accuracy.
This approach is particularly suitable for large datasets, maintaining computational efficiency while enhancing classification performance.
## Conclusion
Integrating LSI with MLPs for text classification effectively reduces dimensionality and preserves semantic relationships in text data. This balance between dimensionality reduction and semantic preservation leads to improved classification accuracy, making it a robust and efficient system for text classification tasks.
