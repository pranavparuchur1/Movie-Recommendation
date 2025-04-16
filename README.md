# Movie Recommendation System

## Description

This project implements a movie recommendation system using three different approaches: user-based collaborative filtering, item-based collaborative filtering, and a graph-based Pixie-inspired algorithm. The system is built using Python and the pandas library.

## Dataset

The MovieLens 100K dataset is used, which contains 100,000 ratings from 943 users on 1682 movies. The dataset includes user IDs, movie IDs, ratings, timestamps, movie titles, and user demographics. The dataset is available at \[MovieLens Dataset Link].

## Methodology

*   **User-based collaborative filtering:** This approach recommends movies to a user based on the preferences of similar users. User similarity is calculated using cosine similarity on the user-movie rating matrix.
*   **Item-based collaborative filtering:** This approach recommends movies that are similar to movies a user has liked. Item similarity is calculated using cosine similarity on the transposed user-movie rating matrix.
*   **Random-walk-based Pixie algorithm:** This approach represents user-movie interactions as a graph and uses random walks to recommend movies. The algorithm starts at a user or movie node and randomly walks through the graph, recommending movies that are frequently visited during the walk.

## Implementation Details

The project is implemented in Python using the pandas library. The main steps include:

1.  Loading the data from the `u.data`, `u.item`, and `u.user` files.
2.  Cleaning the data by handling missing values and converting timestamps.
3.  Creating a user-movie rating matrix using the `pivot()` function.
4.  Implementing user-based and item-based collaborative filtering using cosine similarity.
5.  Constructing an adjacency list graph for the Pixie-inspired algorithm.
6.  Implementing the weighted random walk-based recommendation algorithm.

## Results

The system provides movie recommendations based on the three different approaches. The user-based approach recommends movies based on similar users' preferences. The item-based approach recommends movies similar to those a user has liked. The Pixie algorithm explores the user-movie graph to find relevant recommendations.

## Usage

1.  Download the MovieLens 100K dataset.
2.  Place the dataset files (`u.data`, `u.item`, `u.user`) in the same directory as the `Movie_Recommendation.ipynb` notebook.
3.  Open the notebook using Jupyter Notebook or JupyterLab.
4.  Run the notebook cells to load the data, train the models, and generate movie recommendations.

## Dependencies

*   Python 3.6 or higher
*   pandas
*   scikit-learn
