
MOVIE RECOMMENDER SYSTEM


This project is a Movie Recommender System utilizing the TMDB dataset from Kaggle, which consists of two CSV files: `movies` and `credits`.

## Project Overview

The aim of this project is to use the provided data to create tags for each movie and calculate the distance between these tags to recommend the top 5 movies most similar to a given movie. By leveraging various attributes from the dataset, we generate meaningful tags that help in determining the similarity between movies.

## Key Features

- Data Utilization: The TMDB dataset includes comprehensive information about movies and their credits. We utilize this data to extract relevant features and generate tags for each movie.

- Tag Generation: Tags are created for each movie by combining different attributes such as genres, cast, crew, and more. These tags represent the key characteristics of each movie.

- Similarity Calculation: We calculate the distance between the tags of movies to measure their similarity. This involves using appropriate algorithms to ensure accurate recommendations.

- Top 5 Recommendations: Based on the calculated distances, the system recommends the top 5 movies that are closest in similarity to the given movie.

## How It Works


1. Data Preprocessing:
    - Data Loading and Merging: Load the `movies` and `credits` CSV files from the TMDB dataset and merge 	these two data frames to create a unified dataset.
    - Column Selection: Select relevant columns and drop the rest. The chosen columns are:
        - Genres
        - Id
        - Keywords
        - Title
        - Overview
        - Cast
        - Crew
    - Data Cleaning: Clean the data to handle missing values, inconsistencies, and other preprocessing 	tasks necessary to prepare the data for analysis.

2.Vectorization of Tags:
    - Text to Vector Conversion: Use stemming techniques to handle the problem of text vectorization. 	Implement the Bag of Words technique:
        - Bag of Words: Join all 5000 tags and count the most common words after removing stop words 	(e.g., "is", "the", etc.).
        - Vector Creation: Count the occurrence of the most common words in all tags to create vectors.
        - This can be accomplished using the Scikit-learn library.

3. Model Building:
    - Distance Calculation: Instead of using Euclidean distance in high-dimensional space, calculate 	cosine distance to measure similarity.
    - Recommendation Function: Create a function that uses cosine distance to recommend the top 5 	nearest movies based on the calculated similarities.
    - Integration: Use PyCharm to integrate the model into a website, providing a user-friendly 	interface for movie recommendations.

This project demonstrates the use of data preprocessing, text vectorization, and machine learning techniques to build an effective movie recommender system, providing users with personalized movie suggestions based on their preferences.
