# IMDB Sentiment Analysis with BERT

## Introduction

This project explores sentiment analysis on IMDB movie reviews using BERT (Bidirectional Encoder Representations from Transformers), a powerful language model. The goal is to classify reviews as either positive or negative.

## Goals

- Understand the basics of BERT and how it's used for sentiment analysis.
- Fine-tune a pre-trained BERT model to improve accuracy on the IMDB dataset.
- Compare the performance of a fine-tuned BERT model to a simple Dense Network.

## Methods

1. **Data Preparation:**
   - Loaded the IMDB movie review dataset.
   - Performed data cleaning and preprocessing, including tokenization using the `AutoTokenizer` from HuggingFace.
   - Split the data into training and testing sets.

2. **BERT Model:**
   - Utilized a pre-trained `bert-tiny` model from HuggingFace.
   - Extracted sentence embeddings using the `last_hidden_state` of the model's output.
   - Reduced the data by selecting the embedding corresponding to the `[CLS]` token.

3. **Classification:**
   - Trained a simple Dense Network using the extracted embeddings as features.
   - Fine-tuned the `bert-tiny` model for sequence classification.

## Results

- The fine-tuned BERT model achieved a higher accuracy compared to the simple Dense Network, demonstrating the effectiveness of fine-tuning for sentiment analysis tasks.
- To see the specific accuracy values, refer to the output of the evaluation cells in the notebook.

## Future Improvements

- Experiment with larger BERT models for potentially better performance.
- Explore different fine-tuning strategies and hyperparameters.
- Investigate the use of data augmentation techniques to enhance the model's robustness.

## Conclusion

This project showcased the application of BERT for sentiment analysis on IMDB movie reviews. The fine-tuned BERT model achieved promising results, highlighting its potential for this task. Future work could focus on further improving accuracy and exploring other applications of BERT in natural language processing.
