# fake-news-detector


# Overview

This project is a machine learning-based web application that classifies news articles as Real or Fake. It uses a Passive Aggressive Classifier trained on labeled datasets and deployed through a Streamlit interface for interactive use.

The system focuses on a simple and efficient pipeline using TF-IDF vectorization and a linear model rather than complex deep learning or advanced NLP architectures.

# Key Idea

Instead of using heavy NLP models, this project relies on:

Converting text into numerical features using TF-IDF
Training a fast and effective linear classifier
Deploying the model in a lightweight web app
Features
Interactive web interface built with Streamlit
Real-time fake news prediction
Lightweight and fast model inference
Simple dataset preparation pipeline
Clean separation of training and deployment


# How It Works
1. Dataset Preparation

The project uses two datasets:

True.csv → Real news
Fake.csv → Fake news

The script combine.py:

Adds labels (REAL, FAKE)
Merges both datasets
Shuffles the data
Saves a combined dataset (news.csv)
2. Feature Extraction
Text data is converted into numerical form using TF-IDF vectorization
This captures word importance without complex linguistic processing
3. Model Training
A Passive Aggressive Classifier is trained on the vectorized data
This model is well-suited for text classification and large datasets
The trained model is saved as:
fake_news_model.pkl
tfidf_vectorizer.pkl
4. Deployment (Streamlit App)

The app.py file:

Loads the trained model and vectorizer
Accepts user input (news text)
Transforms input using TF-IDF
Predicts whether the news is REAL or FAKE
Displays the result instantly

# Technologies Used
Python
Scikit-learn
Pandas
Streamlit
Pickle (for model serialization) 


