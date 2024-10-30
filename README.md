# Turkish News Classification Project

## Overview
This project aims to classify Turkish news articles into various categories using state-of-the-art natural language processing (NLP) models: BERT, ELECTRA, and GPT-2. The classification is based on the TR-News dataset, which contains a diverse collection of Turkish news articles.

## Objectives
- Accurately classify Turkish news articles into relevant categories.
- Analyze the performance of different NLP models.
- Identify challenging categories and develop strategies to improve classification accuracy.

## Dataset
The dataset used in this project is the TR-News dataset. Key preprocessing steps included:
- Cleaning and grouping categories to reduce the number of classes.
- Removing certain categories to focus on specific news topics.
- Limiting the dataset to 50,000 samples.

### Final Categories
- Türkiye
- Dünya
- Spor
- Ekonomi
- Sağlık
- Kültür-Sanat
- Eğitim
- Teknoloji

## Model Architecture
The following models were used for the classification task:
1. **BERT**: `dbmdz/bert-base-turkish-cased`
2. **ELECTRA**: `dbmdz/electra-base-turkish-cased-discriminator`
3. **GPT-2**: `ytu-ce-cosmos/turkish-gpt2-large`

### Training Parameters
- Number of epochs: 3
- Learning rate: 2e-5
- Weight decay: 0.01
- Batch sizes: 32 for BERT and ELECTRA, 16 for GPT-2

## Results
The models were evaluated on a validation set with the following accuracies:
- **BERT**: 88.27%
- **ELECTRA**: 87.25%
- **GPT-2**: 88.83%

## Discussion
- **Performance**: GPT-2 achieved the highest accuracy, while all models excelled in the "Spor" category.
- **Challenges**: The "Teknoloji" and "Kültür-Sanat" categories presented classification difficulties.
- **Insights**: BERT and ELECTRA performed similarly, with BERT having a slight advantage.

## Conclusion
The project demonstrates the effectiveness of large pre-trained language models for Turkish news classification. Future work could explore ensemble methods, hyperparameter tuning, and the application of recent models like GPT-3 or T5.

## Requirements
- Python 3.x
- Hugging Face Transformers library
- PyTorch or TensorFlow

## Installation
To install the necessary libraries, run:
```bash
pip install transformers torch  # For PyTorch
# or
pip install transformers tensorflow  # For TensorFlow
