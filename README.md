# Movie Recommender System

This project implements a movie recommender system using content-based and collaborative filtering techniques. The recommender system suggests movies to users based on their preferences and similarities between movies.

## Introduction

The movie recommender system uses both content-based and collaborative filtering methods to provide movie recommendations. Content-based filtering suggests movies similar to a given movie based on their descriptions, keywords, cast, director, and genres. Collaborative filtering recommends movies to a user based on the preferences of similar users.

## Data

The project utilizes the following datasets:

- `movies_metadata.csv`: Contains movie metadata such as title, overview, tagline, genres, etc.
- `credits.csv`: Includes information about movie credits, including cast and crew.
- `keywords.csv`: Contains keywords associated with each movie.
- `links_small.csv`: Provides mapping between movie IDs and external IDs.
- `ratings_small.csv`: Includes user ratings for movies.

## Content-Based Recommender

The content-based recommender uses the movie descriptions, taglines, keywords, cast, director, and genres to calculate similarities between movies. It employs TF-IDF vectorization and cosine similarity to measure the similarity between movies based on their textual features.

## Collaborative Filtering

The collaborative filtering approach uses the Surprise library to build a collaborative filtering model based on matrix factorization. It predicts movie ratings for users based on their historical ratings and recommends movies with high predicted ratings.

## Hybrid Model

The hybrid model combines the content-based and collaborative filtering approaches to provide personalized movie recommendations. It considers both the content-based similarities and the collaborative filtering predictions to suggest movies to users.

## Installation

To run the movie recommender system, follow these steps:

1. Install the necessary packages: Pandas, NumPy, Scikit-learn, NLTK, Surprise. You can install them using pip or use colab to host your notebook.

2. Download the following datasets:
- `movies_metadata.csv`
- `credits.csv`
- `keywords.csv`
- `links_small.csv`
- `ratings_small.csv`

3. Place the downloaded datasets in the same directory as the project files.

## Usage

1. Open the Python script or Jupyter Notebook file that contains the movie recommender system code.

2. Run the code cells or execute the script to load the data and build the recommender system.

3. Use the provided functions to get movie recommendations based on different approaches. For example:
```python
get_recommendations('Toy Story').head(10)
get_recommendations('Asoka').head(10)
hybrid(5, 'Asoka')
hybrid(700, 'Asoka')

