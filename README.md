# Disater-Response-Pipelines Summary
### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [Project Overview](#descriptions)


## Installation <a name="installation"></a>

All libraries are available in Anaconda distribution of Python. Use key libraries are:

- pandas
- re
- sys
- json
- sklearn
- nltk
- sqlalchemy
- pickle
- Flask
- plotly
- sqlite3

The code should run using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

The goal of the project is to classify the disaster messages into categories. 
In this project, I analyzed disaster data from [Figure Eight](https://www.figure-eight.com/) to build a model for an API that classifies disaster messages. 
Through a web app, the user can input a new message and get classification results in several categories along with visualizations of the data. 


## Project Descriptions<a name = "descriptions"></a>
The project has three components: 

1. **ETL Pipeline:** `process_data.py` file contain the script to create ETL pipline which:

- Loads the `messages` and `categories` datasets
- Merges the two datasets
- Cleans the data
- Stores it in a SQLite database

2. **ML Pipeline:** `train_classifier.py` file contain the script to create ML pipline which:

- Loads data from the SQLite database
- Splits the dataset into training and test sets
- Builds a text processing and machine learning pipeline
- Trains and tunes a model using GridSearchCV
- Outputs results on the test set
- Exports the final model as a pickle file

3. **Flask Web App:** the web app enables the user to enter a disaster message, and then view the categories of the message.

The web app also contains some visualizations that help users understand more about the data 


