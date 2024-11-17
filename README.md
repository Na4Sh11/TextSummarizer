# Text Summarization using Huggingface model




This repository contains a Natural Language Project for summarizing the text using Tokenizer.






## About the Dataset


 The Dataset is available on : 

                       https://github.com/DivyanshKushwaha/Dataset/raw/main/summarizer-data.zip

The SAMSum dataset contains about 16k messenger-like conversations with summaries. Conversations were created and written down by linguists fluent in English.

Linguists were asked to create conversations similar to those they write on a daily basis, reflecting the proportion of topics of their real-life messenger convesations. The style and register are diversified - conversations could be informal, semi-formal or formal, they may contain slang words, emoticons and typos.

Then, the conversations were annotated with summaries. It was assumed that summaries should be a concise brief of what people talked about in the conversation in third person. The SAMSum dataset was prepared by Samsung R&D Institute Poland and is distributed for research purposes (non-commercial licence: CC BY-NC-ND 4.0).


## Model Used

- google/pegasus-cnn_dailymail




## Project Structure
This project is organized as follows:

- #### .gitignore
  This file specifies which files and directories should be ignored by Git.
- #### artifacts
     This folder contains the train,test and raw csv files along with the preprocessed and best model pickle file. These files are in this folder:
    - data_ingestion.py
    - data_transformation.py
    - data_validation.py
    - model_trainer.py
    - model_evaluation.py
- #### config
    This folder contains the artifacts files parameters like root directory, file path where the data is to be stored.
- #### logs
    This file helps us to record and manage application events and information, facilitating debugging and monitoring.
- #### research
    This directory contains Jupyter notebooks used for data exploration, visualization and model training. The coding of Data Ingestion to Model Training is done in this directory.
- #### src
    - This directory contains the source code for the project. The envoirement 'projectml' is created under this directory.  
    - Under the directory 'projectml' , there subdirectories are given:
        - components : Source coding of artifacts files is done here. Many classes are created here like logging status , downloading , unzipping etc.
        - config : All config classes are created here.
        - constants : Constants like config_file_path, parameter_file_path are created here that we can use anywhere in the envoirement.
        - entity : All dataclasses of config.yaml are created here.
        - pipeline : This directory contains data processing or machine learning pipelines used in the project, including:
            -  data_ingestion_pipeline.py : Handles the process of loading and preparing the dataset.
            -  data_validation_pipeline.py : Validate the ingestion process.
            -  data_transformation_pipeline.py : Performs data preprocessing and feature engineering.
            -  model_trainer_pipeline.py : Defines the training pipeline for model development.
            -  model_evaluation_pipeline.py : Defines the training pipeline for model development.
            -  prediction_pipeline.py : Defines the pipeline for making predictions using the trained model.
        - utils : Contains utility functions used throughout the project.

 - #### static
     All helping files to build the application functional is here.

 - #### templates
     This folder contains the HTML files used for obtaining user input via form and flask uses these files as a rendering template

 - #### app.py
     This is the Flask application file responsible for hosting the web application.

 - #### main.py
     By running this file in terminal we can start the pipeline or the whole developement that initates from data_ingestion and ends with model_prediction. 

 - #### params.yaml
     It stores the parameter of the machine learning model or algorithm.

  - #### README.md
     This file is an outcome of displaying the projects documentation.

  - #### requirements.txt
     This file lists all the Python libraries and dependencies required to run the project.

  - #### setup.py
     This is the setup file for the project, which may include additional configuration settings.
   
  - #### template.py
     By running this file in terminal we can create a file or folder throughout the project by adding in the list.


## Getting started
 To get started with this project, follow these steps:

  - Create an envoirement 'summarizer' using the following command 

         conda create -n summarizer python=3.9.19

  - Activate the envoirement using the following command:

         conda activate summarizer
 
 

  - Clone the repostiory to your local machine using the following command:

        https://github.com/DivyanshKushwaha/Text-Summarization.git
 
  - Navigate to the project directory:

         cd Text-Summarization

  - We can manually create files and folders mentioned in the template.py. Also we can Create the template.py files and folders using the command:

         python template.py


  - Install the required dependencies using pip:

         pip install -r requirements.txt
    
  - Run the Flask application:

         python app.py


  - Open your web browser and go to given address. Fill the feature values and get the wine quality prediction. 

          http://0.0.0.0:8080
      


## Usage
 This project can be used in summarizing the text as it gives the context of the entered text. It can be a sentence or a paragraph.


## Contributing
 Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

  - Fork the repository.
  - Create a new branch for your feature or bug fix:

        git checkout -b feature-name.
  - Make your changes and commit them:
  
        git commit -m 'Description of your changes'.
  - Push your changes to your fork:
  
        git push origin feature-name.
  - Create a pull request on the original repository.




