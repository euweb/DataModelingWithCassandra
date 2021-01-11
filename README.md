# DataModelingWithCassandra

This project allows Sparkify employees to get analytics from the usage of their app. For this purpose the data engineers at Sparkify developed an Apache Cassandra NoSQL database.

## Queries to be answered

  1.  Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4

  2.  Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userId = 10, sessionId = 182

  3.   Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'

## ETL and Data Modeling

The data is stored in multiple CSV files partitioned by date. First the CSV files are combined together and unnecessary columns are cleaned up. Second the database and the tables are created and filled with data from the combined csv file. Than we run queries on the database. 

## Running using Docker

1. clone this repository
2. run `docker-compose up`
3. start jupyter lab:
    - search in the terminal for connection url like `http://127.0.0.1:8888/?token=f4a438dfe17abe6a80b098d08249b55700f79613ecc7a7da`
    - run _InstallDependencies.ipynb_ notebook to install required dependencies
    - run _Project_1B_ Project_Template.ipynb_ to create tables, import data and run queries