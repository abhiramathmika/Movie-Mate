# Movie-Mate
The objective of the project is to build a content-based movie recommender system that suggests movies to users based on their input. The system leverages cosine similarity to measure the similarity between movies based on their features.

Methodology
Data Collection:

Gather a dataset containing information about various movies. This dataset should include features such as movie titles, genres, plot summaries, cast, directors, and keywords.
Feature Extraction:

Extract relevant features from the dataset. These features could include text-based data (e.g., plot summaries, keywords) and categorical data (e.g., genres, cast).
Used Bag of words to convert text-based data into numerical vectors.
Cosine Similarity Calculation:

Compute the cosine similarity between movie vectors. Cosine similarity measures the cosine of the angle between two vectors, providing a similarity score between 0 and 1.
Higher similarity scores indicate more similar movies.
Recommendation Generation:

For a given movie, identify the most similar movies based on their cosine similarity scores.
Recommend the top N(here N is 5) most similar movies to the user.
Implementation Steps
Data Preprocessing:

Clean and preprocess the dataset to handle missing values and standardize formats.
Tokenize and vectorize text data using bag of words.
Model Building:

Calculate vectors for all movies in the dataset.
Compute cosine similarity between these vectors.
Recommendation Algorithm:

Create a function to fetch the top N similar movies for a given movie based on cosine similarity scores.
User Interface:

Develop a simple user interface where users can input a movie they like and receive recommendations.
Display the recommended movies with relevant information such as titles, genres, and plot summaries.
Example
Suppose a user inputs the movie "Inception". The recommender system will:

Extract the features of "Inception".
Calculate the cosine similarity between "Inception" and all other movies in the dataset.
Rank the movies based on their similarity scores.
Recommend the top N movies that are most similar to "Inception".
Tools and Technologies
Programming Language: Python
Libraries: pandas, scikit-learn, numpy, nltk (for text processing), Streamlit (for web interface)
