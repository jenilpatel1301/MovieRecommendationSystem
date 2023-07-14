# MovieRecommendationSystem

This repository contains code for a movie recommendation system implemented using Python and machine learning techniques. The recommendation system suggests similar movies based on the user's input.

## Table of Contents

- [Dependencies](#dependencies)
- [Data](#data)
- [Usage](#usage)
- [Recommendation Algorithm](#recommendation-algorithm)
- [Example](#example)

## Dependencies

The following Python libraries are required to run the recommendation system:

- numpy
- pandas
- nltk
- sklearn

You can install these libraries using pip:

```
pip install numpy pandas nltk scikit-learn
```

## Data

The movie recommendation system uses the TMDB 5000 Movie Dataset, which includes information about movies such as budget, genres, keywords, cast, crew, and more. The dataset is split into two CSV files: `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`.

To run the recommendation system, make sure to place these CSV files in the same directory as the Python scripts.

## Usage

To use the movie recommendation system, follow these steps:

1. Install the required dependencies mentioned in the [Dependencies](#dependencies) section.
2. Download the TMDB 5000 Movie Dataset and place the CSV files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) in the same directory as the Python scripts.
3. Run the Python script `recommendation_system.py`.
4. Follow the prompts to enter a movie title.
5. The system will recommend similar movies based on the input.

## Recommendation Algorithm

The movie recommendation system uses the following algorithm:

1. Preprocess the movie dataset by cleaning and transforming the data.
2. Extract relevant features from the dataset, such as movie title, overview, genres, keywords, cast, and crew.
3. Combine these features into a single "tags" column, which represents the characteristics of each movie.
4. Apply text preprocessing techniques, including stemming and converting to lowercase, to the "tags" column.
5. Use the CountVectorizer from scikit-learn to convert the text data into numerical vectors.
6. Compute the cosine similarity between the vectors of each movie pair.
7. Based on the user's input movie, recommend the most similar movies by sorting the cosine similarity scores in descending order.

## Example

Here's an example of how to use the movie recommendation system:

1. Run the `recommendation_system.py` script.
2. Enter the movie title: "The Dark Knight Rises".
3. The system will recommend similar movies based on the input.
