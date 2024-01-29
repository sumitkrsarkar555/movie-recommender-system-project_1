# Movie Recommendation System

## Table of Contents

- [Problem Statement](#problem-statement)
- [Business Understanding](#business-understanding)
- [Business Goal](#business-goal)
- [Dataset](#dataset)
- [Project Pipeline](#project-pipeline)
    - [Importing Libraries](#importing-libraries)
    - [Data Reading](#data-reading)
    - [Data Information](#data-information)
    - [Data Preprocessing and Cleaning](#data-preprocessing-and-cleaning)
    - [Data Modeling and Model Training](#data-modeling-and-model-training)
    - [Test the Model](#test-the-model)
- [Technology Used](#technology-used)
- [Acknowledgments](#acknowledgments)

## Problem Statement

Traditional movie recommendation systems often rely on basic criteria like genre and popularity, leading to inaccurate recommendations that do not reflect the user's personal preferences. This results in a poor user experience. Therefore, there is a need for a more personalized and accurate movie recommendation system that considers a user's individual taste and viewing history.

## Business Understanding

A movie recommendation system can provide a significant advantage for streaming platforms by offering personalized recommendations. This helps in retaining users, increasing engagement, informing content acquisition decisions, and ultimately boosting revenue.

## Business Goal

Develop a movie recommendation system that provides personalized suggestions based on individual user taste and viewing history.

## Dataset

This project utilizes the TMDB 5000 movie dataset acquired from Kaggle.
- Link: [TMDB Movie Metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
- Dataset contains 20 columns and 4802 rows.

## Project Pipeline

### Importing Libraries
- Importing different libraries and dependencies to execute the project on Google Colab.

### Data Reading
- Upload the dataset downloaded from Kaggle and copy the dataset path.

### Data Information
- Utilize `head()` and `tail()` functions to understand essential columns.
- Use `describe()` to analyze mean, min, and max functions.
- Display columns and datatypes of each column.

### Data Preprocessing and Cleaning
- Handle missing values using `isnull()` function.
- Select relevant columns such as 'id', 'title', 'overview', and 'genre'.
- Drop unnecessary columns like 'overview' and 'genre'.
- Import CountVectorizer from sklearn.
- Extract the 'tag' column from the DataFrame ('new_data') and convert it to a NumPy array of Unicode strings ('U').

### Data Modeling and Model Training
- Import CountVectorizer from sklearn.
- Create CountVectorizer with specific parameters.
- Import cosine similarity from sklearn.
- Train the similarity vector using cosine similarity.

### Test the Model
- Select a random title from the dataset.
- Find the index value of the title.
- Use cosine similarity to find 5 similar values close to the chosen title.
- Use the difflib library and an if-else function to find the closely matched input of user input. This accounts for variations in capitalization, spelling mistakes, or other discrepancies.
  
## Technology Used

- Google Colab
- NumPy
- pandas
- difflib library
- CountVectorizer
- scikit-learn (cosine similarity)

## Acknowledgments

The TMDB 5000 Movie Dataset was acquired from Kaggle ([TMDB Movie Metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)).

