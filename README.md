# SVD-Based Text Classification

## Problem Statement
Automatic text classification is essential for retrieving information and organizing tasks in various applications like sentiment analysis, document categorization, and spam detection. However, dealing with high-dimensional text data poses significant computational challenges and can affect classification performance. This project explores the use of Latent Semantic Indexing (LSI), leveraging Singular Value Decomposition (SVD), to reduce dimensionality while preserving semantic relationships in text data for improved classification accuracy.

## Project Architecture
This project utilizes the Reuters dataset 
- **Data Collection:** The Reuters Corpus Volume 1 (RCV1) is used, containing news articles with metadata fields like region codes, industry codes, and topic codes.
- **Data Preprocessing:** Text data is cleaned, normalized, and structured through a series of preprocessing steps, including text expansion, tokenization, stop word removal, punctuation removal, and lemmatization.
- **Document Representation:** Text data is converted into a numerical format using Term Document Matrix (TDM) and count vectorization.
- **Dimensionality Reduction:** LSI, based on SVD, is applied to reduce the dimensionality of the TDM, capturing the underlying semantic structure of the document collection.
- **Classification Model:** Multi-Layer Perceptrons (MLPs) are used as the classification model to learn complex non-linear relationships in the data.
