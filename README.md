# Book Recommendation System 📚

<div align="left">

[![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/pandas-%23150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-%23013243?style=flat-square&logo=numpy&logoColor=white)](https://numpy.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E?style=flat-square&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![IPython](https://img.shields.io/badge/IPython-%230C55A5?style=flat-square&logo=ipython&logoColor=white)](https://ipython.org/)
[![ipywidgets](https://img.shields.io/badge/ipywidgets-%23444?style=flat-square&logo=ipywidgets&logoColor=white)](https://ipywidgets.readthedocs.io/)

</div>

This repository contains Python code for building a book recommendation system. The system uses techniques like TF-IDF (Term Frequency-Inverse Document Frequency) and cosine similarity to provide book recommendations based on user input.

## Prerequisites

Before running the code, make sure you have the following prerequisites installed:

- **Python Libraries**: You'll need the following Python libraries, which can be installed using pip:
   - `numpy` for numerical operations.
   - `pandas` for data manipulation.
   - `re` for text cleaning.
   - `sklearn.feature_extraction.text` for TF-IDF vectorization.
   - `sklearn.metrics.pairwise` for cosine similarity calculation.
   - `ipywidgets` for creating interactive widgets.
   - `IPython.display` for displaying recommendations.

## Code Overview

### 1. Loading Data

The code begins by loading book data from a CSV file called `movies.csv`. This dataset includes information about book titles and genres.

Note: In this notebook we used a large file Datas. So, if you need to [download](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmtHS3EwY21CVVNLbkZFQ1NrQUNkTXpMeFpUUXxBQ3Jtc0ttUkN5Y1RQWTdFbVBzTFRkNlE5MWd1STc5Z2JXSHE4VUtuaFBhdHpIRTBfTmNheUpqbm9jY0R6XzZ6ZHZDeDBrZEpQTmZqRG5LSG5rZGV0U1BZYnBlWE4tOTlXQnlfQy11UVAxdWZzejBWdEJwczhvTQ&q=https%3A%2F%2Ffiles.grouplens.org%2Fdatasets%2Fmovielens%2Fml-25m.zip&v=eyEabQRBMQA) Data, Feel Free too.

### 2. Building the Search Engine 🚂

- **Cleaning the Book Title**: The `clean_text` function cleans book titles by removing special characters and converting the text to lowercase.

- **Creating a TF-IDF Matrix**: TF-IDF vectorization is performed on the cleaned book titles to convert them into numerical vectors.

- **Creating a Search Function**: The `search` function takes a user's book title query, converts it into a vector, and calculates cosine similarity with other book titles. It returns the top 5 book recommendations based on similarity.

### 3. User Input and Display

- **User Input**: Users can input a book title into an interactive widget. The input is processed, and recommendations are displayed dynamically.

- **Display Recommendations**: Recommendations are displayed as a list of book titles and genres.

### 4. Creating Recommendation Function

- **Loading Rating Data**: The code loads rating data from a CSV file called `ratings.csv`. This dataset contains user ratings for books.

- **Find Similar User**: The `find_similar_user` function takes a book's ID and finds similar users who rated that book highly. It then calculates a recommendation score based on these similar users and all users who rated the book highly.

### 5. User Input and Recommendation Display

- **User Input for Recommendation**: Users can input a book title into another interactive widget. The code finds the most similar book based on the user's query and calculates book recommendations.

- **Display Recommendations**: Recommendations are displayed as a list of book titles and genres.

## Usage

1. Make sure you have all the prerequisites installed.

2. Run the code step by step in a Jupyter Notebook or a similar environment.

3. Input a book title to receive recommendations based on book similarity.

4. Explore the recommendations and discover new books to read!

Feel free to modify the code, dataset, or user interface to tailor the book recommendation system to your needs. Enjoy discovering new books with the recommendation engine! 📚📖
