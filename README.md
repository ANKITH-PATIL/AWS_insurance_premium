# Insurance__Premium_ML_Prediction

Application url:
[Insurance_Premium_Predictor](https://insurance-premiumapp.herokuapp.com/)


This machine learning project predicts the premium of the insurance

```
CI-CD Pipleine:
```

<p align="center">
  <img src="https://d3hi6wehcrq5by.cloudfront.net/itnavi-blog/2021/07/CI-CD-la-gi-1.png"/>

CI: changing your code and sending the changes to the github 
CD: When the deployement criteria satisfies then the trigger is triggered 

I have done continuous deployement to the cloud(heroku) whenever there is something pushed onto the main branch of the GITHUB repository
this trigger is added to the main.yaml file in the workflow of .github file  

```
how to clone from github repo
```
```
create a github repo
go on code and copy the https link of the repo
go to terminal of your system
git clone *paste the link* 
```
```
next steps : edit the repo using the VS code
```
```
type dir in command prompt
type cd *project name*
type code . *for opening the file in the vscode*
```

```
Advantages of maintaining the virtual environment for the project
```
```
its a lighter option than creating a new conda environment because as its stored in the same directory(folder).Thus, when u delete the project from your system the virtual environment also gets deleted
```

```
creating requirements.txt file
```
```
create a simple flask application
check its working for checking the reu=quirements.txt
```
```
to check the versions of the project which is created after every git commit
```
```
git log
```
```
how to deploy the model to heroku
```
```
To setup CI/CD pipeline in heroku we need 3 information
1. HEROKU_EMAIL = ankithpatilbusiness@gmail.com
2. HEROKU_API_KEY = <>
3. HEROKU_APP_NAME = insurance-premiumapp


heroku api key you will get from the the account setting on the heroku website 
```
BUILD DOCKER IMAGE
```
docker --version

docker build -t <image_name>:<tagname> .
```
> Note: Image name for docker must be lowercase


To list docker image
```
docker images
```

Run docker image
```
docker run -p 5000:5000 -e PORT=5000 f8c749e73678
```

To check running container in docker
```
docker ps
```

Tos stop docker conatiner
```
docker stop <container_id>
```

```
NEXT STEPS :
```
```
create a folder .github
and within that folder make another folder of workflows
and within that create main.yaml file 

then add readymade template to that file

then add the secrets to your github account(in settings>> secrets>> actions>> new repo secrets) to make sure that whatever secrets u have put in the main.yaml file for the deployemnet of the contd deployement of the(changes u have done to the code) contd integration. 
```

create a new folder based on the name 0f the project(insurance)

create a new  file named (setup.py)
# importance of using a setup file 

## Table of contents
* [About project](#about-project)
* [Technologies](#technologies)
* [Software and account requirement](#software-and-account-requirement)
* [Setup](#setup)
* [Project Pipeline](#project-pipeline)
<!-- * [License](#license) -->

## About project
This app predicts Insurance premium price based on some data.


## Technologies
This project is created with below technologies/tools/resorces:
* Python: 3.7
* Machine Learning
* Jupyter Notebook
* HTML/CSS
* Docker
* Git
* CI/CD Pipeline
* Heroku


## Software and account Requirement
1. [Github Account](https://github.com/)
2. [Heroku Account](https://id.heroku.com/login)
3. [VS Code IDE](https://code.visualstudio.com/download)
4. [GIT CLI](https://git-scm.com/downloads)


## Setup
Create a conda environment
```
conda create -p venv python==3.7 -y
```

activate conda environment
```
conda activate venv/
```

To install requirement file
```
pip install -r requirements.txt
```

* Add files to git  `git add .` or  `git add <file_name>`    
* To check the git status  `git status`    
* To check all version maintained by git  `git log`    
* To create version/commit all changes by git  `git commit -m "message"`    
* To send version/changes to github  `git push origin main`    


## Project Pipeline
1. [Data Ingestion](#1-data-ingestion)
2. [Data Validation](#2-data-validation)
3. [Data Transformation](#3-data-transformation)
4. [Model Training](#4-model-training)
5. [Model Evaluation](#5-model-evaluation)
6. [Model Deployement](#6-model-deployement)

### 1. Data Ingestion: 
* Data ingestion is the process in which unstructured data is extracted from one or multiple sources and then prepared for training machine learning models.

### 2. Data Validation:
* Data validation is an integral part of ML pipeline. It is checking the quality of source data before training a new mode
* It focuses on checking that the statistics of the new data are as expected (e.g. feature distribution, number of categories, etc). 

### 3. Data Transformation 
* Data transformation is the process of converting raw data into a format or structure that would be more suitable for model building.
* It is an imperative step in feature engineering that facilitates discovering insights.

### 4. Model Training
* Model training in machine learning is the process in which a machine learning (ML) algorithm is fed with sufficient training data to learn from.

### 5. Model Evaluation
* Model evaluation is the process of using different evaluation metrics to understand a machine learning model’s performance, as well as its strengths and weaknesses.
* Model evaluation is important to assess the efficacy of a model during initial research phases, and it also plays a role in model monitoring.

### 6. Model Deployement
* Deployment is the method by which we integrate a machine learning model into production environment to make practical business decisions based on data.
 

<p align="center">
  <img src="https://algorithmia.com/blog/wp-content/uploads/2020/09/ML-Pipeline-1_A-scaled.jpg"/>



