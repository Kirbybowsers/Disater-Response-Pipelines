# Disater-Response-Pipelines Summary
### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Description](#descriptions)
4. [Instruction](#descriptions)
5. [Licensing, Authors, Acknowledgements](#licensing)


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


## File Description<a name = "descriptions"></a>
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
Here is a screemshot of one of the graphs: 

![project graph1](ss_1.jpg)


## Instructions:<a name="instructions"></a>
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/


## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Credits must be given to Udacity for the starter codes and FigureEight for provding the data used by this project. 
