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
   
## Queries and Tables

#### 1. Give me the artist, song title and song's length in the music app history that was heard during  sessionId = 338, and itemInSession  = 4

Creating music_history table  
 -  session_id int    
 -  item_in_session int    
 -  artist_name text    
 -  song_title text    
 -  song_length decimal    

I used session_id and item_in_session as PRIMERY KEY because they asked to have list of information that was filtered by session_id and item_in_session.

#### 2. Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
    
Creating user_songs table    
 -  user_id int     
 -  session_id int     
 -  item_in_session int     
 -  user_f_name text     
 -  user_l_name text     
 -  artist_name text     
 -  song_title text     

I used user_id and session_id as PRIMERY KEY because they asked to have list of information that was filtered by user_id and session_id.     
In addtion, I used item_in_session in PRIMERY KEY to sort the result as they requested.

#### 3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'

Creating user_history table     
 -  song_title text     
 -  user_id int     
 -  user_f_name text     
 -  user_l_name text     

I used song_title and user_id as PRIMERY KEY because they asked to have list of information that was filtered by song_title and user name (first and last).     
Note: I could not use user name (first and last) as PRIMERY KEY because sometime you can find two or more people with same first  and last name.
