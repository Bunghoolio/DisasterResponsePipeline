# Disaster Response Pipeline Project

##Table of contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Instructions](#instructions)
5. [Licensing, Authors, and Acknowledgements](#licensing)

### Installation <a name ='installation'></a>

### Project Motivation <a name ='motivation'></a>

### File Descriptions <a name ='files'></a>




### Instructions: <a name ='instructions'></a>
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/ or to http://localhost:3001/
# DisasterResponsePipeline

### Licensing, Authors, and Acknowledgements <a name ='licensing'></a>
