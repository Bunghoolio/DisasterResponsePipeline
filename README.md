# Disaster Response Pipeline Project

## Table of contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name ='installation'></a>
Besides the libraries coming with Python 3.6 the following libraries had been included in this project:
* Flask
* nltk
* numpy
* pandas
* plotly
* regex
* sklearn
* SQLAlchemy

## Project Motivation <a name ='motivation'></a>

This project was initiated as part of my Udacity Data Science Nano Degree Course.

The dataset used in this project was provided by [Figure Eight Inc.](https://en.wikipedia.org/wiki/Figure_Eight_Inc.). This dataset contains messages that were sent during disaster events via social media.
Leveraging this dataset a ML classifier was built to identify messages and their related events.

Within this project, data cleaning and model building steps were performed leveraging pipelines, GridSearch and process automation. The final model is used in a Flask Web App to enable end users to classify any (English) message against any related disaster event.

## File Descriptions <a name ='files'></a>
### 1. ETL pipeline
The ETL Pipeline performs the following steps:
* loading the messages.csv and categories.csv datasets
* merging both datasets
* cleaning datasets
* storing final dataset into SQLite database

The ETL pipeline is available in this project as a .ipynb-file `.\JupyterWorkspace\ETL Pipeline Preparation.ipynb` and as a .py-file `.\data\process_data.py`

### 2. ML Pipeline
The ML Pipeline performs the following steps:
* loading the data from the SQLite database
* building the parser and ML pipeline
* splitting data into train and test dataset
* training pipeline and performing GridSearchCV
* test pipeline

The ML Pipeline is available in this project as a .ipynb-file `.\JupyterWorkspace\ML Pipeline Preparation.ipynb` and as a .py-file `.\models\train_classifier.py`

### 3. Flask Web App

  1. Run the following commands in the project's root directory to set up your database and model.<br/>
    To run ETL pipeline that cleans data and stores in database<br/>
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`<br/>
    To run ML pipeline that trains classifier and saves<br/>
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`<br/>

  2. Run the following command in the app's directory to run your web app.<br/>
    `python run.py`

  3. Go to http://0.0.0.0:3001/ or to http://localhost:3001/

### Licensing, Authors, and Acknowledgements <a name ='licensing'></a>
I am grateful for the opportunity testing my knowledge within this challenging project provided by Udacity and Figure8. For anyone I was able to inspire by my code, feel free to use the code here as you would like!
