# Twitter Sentiment Analysis Using Machine Learning

## Overview

This project focuses on analyzing sentiment from Twitter posts using a machine learning approach. The model categorizes tweets as either positive or negative based on the content. Logistic regression is used as the machine learning algorithm to classify the tweets, and the project also involves preprocessing the textual data, converting it to numerical form, and evaluating the model's accuracy.

## Project Structure

The following components are included in this project:

1. **Data Preprocessing**:
   - The dataset is loaded from a CSV file that contains pre-processed Twitter data.
   - Stemming and stopword removal are applied to reduce words to their root form and remove common, non-informative words.

2. **Feature Extraction**:
   - The `TfidfVectorizer` is used to convert the text data into numerical representations, making it suitable for the logistic regression model.

3. **Model Training**:
   - Logistic Regression is used to train the model on 80% of the dataset.
   - The accuracy of the model is evaluated on both the training and test data.

4. **Model Persistence**:
   - The trained model is saved using the `pickle` library, allowing for future predictions without needing to retrain the model.

## Dataset

The dataset can be downloaded on Kaggle : https://www.kaggle.com/datasets/kazanova/sentiment140

The dataset used in this project consists of labeled tweets, where the target label is either `0` (negative sentiment) or `1` (positive sentiment). The dataset is loaded from the CSV file `training.1600000.processed.noemoticon.csv`, and it requires an `ISO-8859-1` encoding format. 

### Data Preprocessing Steps:
- The dataset's columns are named (`target`, `id`, `date`, `flag`, `user`, `text`).
- Tweets are cleaned by removing non-alphabetic characters and converting all text to lowercase.
- Stopwords (common English words) are removed, and stemming is applied to reduce words to their base form.

## Model Training and Evaluation

The data is split into training and testing sets using an 80/20 ratio. Logistic Regression is used to classify tweets based on their transformed textual features.

### Accuracy Results:
- The model achieves an accuracy score on both training and test datasets, allowing you to assess how well the model generalizes to unseen data.
