# Disaster Tweet Identification Project

## Overview

This project focuses on developing a machine learning model to accurately identify tweets related to actual disasters. With Twitter being a primary platform for instant communication, distinguishing between emergency-related tweets and non-emergency ones is vital for enhancing emergency responses and timely news reporting. Given the impracticality of manually sorting through the vast volume of social media data, this project aims to automate the process, providing significant benefits to disaster relief organizations and news agencies. This project and the data was a part of a Kaggle competition on [Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started/)

## Data

The dataset comprises a training set with 7,613 entries and a test set with 3,263 entries. Each entry includes a tweet's text along with optional keyword and location data. The training data is labeled with a binary target indicating whether a tweet pertains to a real disaster (`1`) or not (`0`).

## Purpose

The primary goal is to leverage machine learning, specifically natural language processing (NLP) techniques, to filter and classify tweets accurately. This capability is crucial for rapid and reliable disaster response and information dissemination.

## Approach

The project was executed in several steps:

1. **Data Preprocessing**: The text data was cleaned by converting to lowercase, removing special characters, excluding stopwords, and applying lemmatization to reduce words to their base forms.

2. **Exploratory Data Analysis (EDA)**: Initial analysis revealed a significant number of missing values in 'location' and 'keyword' columns, with approximately 43% of the tweets in the training dataset labeled as disaster-related. The most frequent locations and keywords were identified to understand the data better.

3. **Model Architecture**: A sequential model with GRU (Gated Recurrent Unit) layers was chosen for its efficiency in handling temporal dependencies in text sequences. The model included embedding for word representation, GRU layers for sequence processing, dropout layers to prevent overfitting, and dense layers for output, using a sigmoid activation function for binary classification.

4. **Training and Validation**: The model was trained on the preprocessed training data, with class weights applied to address any imbalance. Validation was performed on a split of the training data to monitor the model's performance and adjust parameters as needed.

## Results

The model underwent several iterations with adjustments to the architecture and parameters. Despite achieving only 57% accuracy, the project established a foundational pipeline for NLP classification tasks, particularly in the context of disaster tweet identification. The results indicate potential for improvement with further iteration and refinement.

## Conclusion

This project highlighted the challenges and opportunities in applying deep learning to NLP problems within the domain of disaster response on social media. While the current model's performance is modest, the groundwork laid by this project provides a pathway for future enhancements and applications.

