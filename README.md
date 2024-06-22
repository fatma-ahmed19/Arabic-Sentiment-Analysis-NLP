# Sentiment Analysis of Arabic Social Media Content
This repository contains the implementation of a deep learning model to perform sentiment analysis on Arabic social media content. The project aims to classify the sentiment of text data into positive, negative, and neutral categories using Long Short-Term Memory (LSTM) neural networks.

# Features
## 1) Text Preprocessing:
   - Tokenization
   - Normalization of Arabic text
   - Emoji and emoticon handling
   - Removal of redundant spaces, numbers, and diacritics
   - Removal of repeated characters and words

## 2) Model Architecture:

- Embedding Layer
- LSTM Layer
- Dense Layer with Dropout for regularization

## 3) Training:

- Train/test split
- Early stopping for preventing overfitting -
- Handling class imbalance


# Usage

## Data Preparation:
  - Place your training data in an Excel file named train.xlsx with columns review_description and rating.
  - The review_description column should contain the text data, and the rating column should contain the sentiment labels (-1 for negative, 0 for neutral, 1 for positive).
## Running the Script:
```python
python sentiment_analysis_arabic_social_media.py

```
# Code Explanation
## Text Preprocessing

 The text preprocessing steps are crucial for preparing the Arabic text data for training the model. The preprocessing functions include:

  - normalize_text: Normalizes the Arabic text by replacing certain characters with a standard form.
  - emojiTextTransform: Converts emojis in the text to their corresponding Arabic words.
  - remove_redundant_spaces_number: Removes redundant spaces and numbers from the text.
  - remove_repeated_words_with_order: Removes repeated words while preserving the order of unique words.
  - remove_repeating_chars: Collapses repeated characters to a single instance.

## Model Architecture

The LSTM model is implemented using Keras and consists of the following layers:

  - Embedding Layer: Converts the input text into dense vectors of fixed size.
  - LSTM Layer: Captures the temporal dependencies in the text data.
  - Dense Layer: Performs the final classification into sentiment classes.
  - Dropout Layer: Prevents overfitting by randomly dropping units during training.

## Training

The model is trained using the preprocessed text data. The training process includes:

  - Splitting the data into training and validation sets.
  - Encoding the sentiment labels for multi-class classification.
  - Applying early stopping to terminate training when the validation performance stops improving.

## Results

After training, the model's performance can be evaluated using various metrics such as accuracy, precision, recall, and F1-score. The class distribution of the dataset is also visualized using a pie chart to understand the balance of sentiment classes.
Contributing

Contributions to the project are welcome. If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request.
