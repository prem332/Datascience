markdown
Copy code
# Mental Health Sentiment Analysis

This project utilizes a Bidirectional LSTM model to classify tweets related to mental health into four sentiment categories: positive, negative, neutral, and irrelevant. The dataset is sourced from Twitter via Kaggle, and the project also includes a web application developed using Streamlit to allow users to input a tweet and receive sentiment predictions.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Model](#model)
- [Installation](#installation)
- [Usage](#usage)
- [Web Application](#web-application)
- [Results](#results)
- [Challenges Faced](#challenges-faced)
- [Future Work](#future-work)
- [License](#license)

## Overview

The goal of this project is to analyze sentiment related to mental health on social media. Understanding public sentiment can provide valuable insights for mental health awareness and intervention. This project specifically focuses on tweets labeled with sentiments that can be categorized into one of four classes: positive, negative, neutral, or irrelevant.

## Dataset

The dataset used for training and testing the model was obtained from Kaggle. It contains thousands of tweets labeled with the sentiment they express regarding mental health topics. The classes in the dataset are:

- Positive
- Negative
- Neutral
- Irrelevant

You can find the dataset [here](https://www.kaggle.com/datasets).

## Model

### Bidirectional LSTM

The Bidirectional LSTM (Long Short-Term Memory) model was chosen for its ability to capture contextual information from both the past and future within the tweet. The model was trained with the following features:

- Embedding Layer for word embeddings.
- Bidirectional LSTM layer to process the tweet.
- Dropout layers to prevent overfitting.
- Dense layers with regularization to classify the tweet into one of the four sentiment categories.

### Other Models Considered

- **Random Forest** (Accuracy: 94.6%)
- **Bidirectional LSTM** (Accuracy: 96.20% - selected for deployment)

## Installation

To run the project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/Mental-Health-Sentiment-Analysis.git
   cd Mental-Health-Sentiment-Analysis
Install dependencies:

Ensure you have Python 3.9 or above installed. Then, install the required libraries using the provided requirements.txt file:

bash
pip install -r requirements.txt
Download the dataset:

Place the dataset files into the data folder (or update the path in train_model.py).

Train the model (optional):

If you want to retrain the model, you can run:

bash
python model_training.py
Usage
Once the environment is set up, you can use the sentiment analysis model via the web application or directly through the script.

Running the Web Application
To run the Streamlit web app, use the following command:

bash
streamlit run app.py
This will launch the application in your browser, where you can input a message and get the predicted sentiment.

Web Application
The web application allows users to interact with the trained model. After inputting a tweet or any message related to mental health, the app processes the input and predicts the sentiment based on the trained Bidirectional LSTM model.

Features:
Simple UI where users can enter text.
The sentiment (positive, negative, neutral, or irrelevant) is displayed after submission.
Built using Streamlit.
Results
The Bidirectional LSTM model achieved the following performance:

Accuracy: 96.20%
Test Loss: [Include test loss here]
The model outperformed the Random Forest model (94.6% accuracy), making it a suitable choice for deployment.

Challenges Faced
Class Imbalance
The dataset was imbalanced, with some sentiment categories having significantly fewer samples than others. To address this:

Class weights were used to balance the effect of each class during training.
Early stopping was implemented to prevent overfitting, especially on minority classes.
Optimizing Class Weights
Finding the right balance between classes without degrading the model's performance on the majority classes was a challenge. Class weights initially made the model more prone to overfitting on the minority classes, and careful tuning of hyperparameters was required.

Future Work
Real-time sentiment analysis on live Twitter data.
Incorporating more diverse data sources for better generalization.
Improving the user interface and adding a feedback mechanism to enhance model accuracy based on user inputs.










