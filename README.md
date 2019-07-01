# Project: Data Modeling with Cassandra
## Introduction
A startup called 'Sparkify' wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. Their analysis team is particularly interested in understanding what songs users are listening to. This project will help them to query the data to generate the result by reading the data that reside in a directory of CSV files on user activity on the app.    
In this project, I will create an Apache Cassandra database for this analysis which can create queries on song play data to answer the questions. They can test the new database by running queries 
## Project Description
In this project, I will apply what I have learned on data modeling with Apache Cassandra and complete an ETL pipeline using Python. To complete the project, I will need to model my data by creating tables in Apache Cassandra to run queries.    
They have provided me with a project template that takes care of all the imports and provides a structure for ETL pipeline I'd need to process this data.   
## Datasets
For this project, I am working with one dataset ‘event_data’. The directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:   
- event_data/2018-11-08-events.csv   
- event_data/2018-11-09-events.csv    

## Project Template
The project template includes one Jupyter Notebook file, in which:
   - I will process the event_datafile_new.csv dataset to create a denormalized dataset    
   - I will model the data tables    
   - I will provide queries that I will need to model my data tables 