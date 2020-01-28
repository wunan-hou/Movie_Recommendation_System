# Project Summary
The methodology of this movie recommendation system is based on a similarity comparison between movie contents and attributes. In other words, users may get recommendations for movies based on a series of movie tags, such as movie name, reviews, plots, genres, directors, etc.

# Database
The database is obtained by web scraping IMDb website. It contains 267,581 movies along with 12 attributes - movie name, genre, director, writer, star, keyword, reviews, release country, release date, rating value, and time in csv format.

# Data Visualization
Here, we displayed different graphs to help users better visualize distribution of movie attrbutes, such as the proportion of release country under each movie genre and distributions of rating values by release countries for each genre.

# Text Mining 
## sentiment analysis
Using Vader to assign a “compound” score to reviews for each movie.
## Similarity
Using LSI model to detect similarity between movies.
## Simple analysis: Words Cloud
Combined movie’s keywords, genre, reviews and storyline to generate a word cloud for each movie

# Feature Value
## Binary Attributes
Set director, genres, keywords, release country, release date, stars, storyline, writers as binary independent variables. If they are null, we set the value as 0, otherwise, set as 1.
Assigned compound scores from sentiment analysis to reviews and normalize it.
Set rating values which are larger than 7 as 1, otherwise as 0 to be our dependent variables.
## Numerical Attributes
Taking director attribute as an example, we find all movies of the director and drop out movies without rating value, calculate the average rating and assign this average to the director as his/her numerical value. If all movies of this director don’t have rating values, we set 0 to this director. The same process applies to genres, release country, stars, and writers. Reviews and dependent variable are handled the same way as described in binary attributes.

# Machine Learning
Logistic Regression, Random Forest, Neural Network

# Movie Recommendation
## Using movie attributes to get recommendation
The system supports users to input arbitrary combined movie attributes and return top 10 rating movies.
## Using movie name to get recommendation
The system also support uses to get recommendation solely based on movie names.
