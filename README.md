# DiasterResponse
# Installation
This repository was written in HTML and Python , and requires the following Python packages: pandas, numpy, re, pickle, nltk, flask, json, plotly, sklearn, sqlalchemy, sys, warnings.
# Project Motivation
In this project, we build a ML a model to classify messages that are sent during disasters. It included several examples like Medical Help, Search , Aid Related and Rescue. By classifying these messages, we can allow these messages to be sent to respective diaster agency. Current project involvs in Data analysing perhaps we call it as ETL development and Machine learning pipeline to facilitate the classification task.

# File Description
There are three main foleders:

  1. Data
        disaster_categories.csv: dataset including all the categories
        disaster_messages.csv: dataset including all the messages
        process_data.py: ETL pipeline scripts to read, clean, and save data into a database
        DisasterResponse.db: output of the ETL pipeline, i.e. SQLite database containing messages and categories data
  2. Models
        train_classifier.py: machine learning pipeline scripts to train and export a classifier
        classifier.pkl: output of the machine learning pipeline, i.e. a trained classifer
  3. App
        run.py: Flask file to run the web application
        templates contains html file for the web applicatin
        
# Instructions:

1.  Run the following commands in the project's root directory to set up your database and model.

      a. To run ETL pipeline that cleans data and stores in database python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
      b. To run ML pipeline that trains classifier and saves python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
      
2. Run the following command in the app's directory to run your web app. python run.py
3. Go to http://0.0.0.0:3001/
