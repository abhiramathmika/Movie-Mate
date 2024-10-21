# Movie Mate

Movie Mate is a content-based movie recommender system that suggests movies to users based on their input. The system uses cosine similarity to measure the similarity between movies by analyzing features such as titles, genres, plot summaries, cast, directors, and keywords.

## Objective

The goal of Movie Mate is to provide personalized movie recommendations by leveraging content-based filtering techniques. By calculating the similarity between movies, the system can suggest the top N (in this case, 5) movies that are most similar to a given movie input by the user.

## Methodology

### 1. Data Collection

- **Dataset**: The system uses a movie dataset from TMDB, which contains information about various movies. The dataset includes features such as movie titles, genres, plot summaries, cast, directors, and keywords.
- **Dataset Link**: [TMDB Movie Metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

### 2. Feature Extraction

- Extract relevant features from the dataset, including text-based data (e.g., plot summaries, keywords) and categorical data (e.g., genres, cast).
- Use the Bag of Words technique to convert text-based features into numerical vectors.

### 3. Cosine Similarity Calculation

- Compute the cosine similarity between movie vectors to measure the similarity between two movies. Cosine similarity scores range from 0 to 1, with higher scores indicating more similarity.

### 4. Recommendation Generation

- For a given movie, identify the top N most similar movies based on their cosine similarity scores.
- Recommend the top 5 most similar movies to the user.

## Implementation Steps

### 1. Data Preprocessing

- Clean and preprocess the dataset to handle missing values and standardize formats.
- Tokenize and vectorize text data using the Bag of Words model.

### 2. Model Building

- Calculate vectors for all movies in the dataset using the extracted features.
- Compute cosine similarity between these vectors to measure movie similarity.

### 3. Recommendation Algorithm

- Implement a function to fetch the top 5 similar movies for a given movie based on cosine similarity scores.

### 4. User Interface

- Develop a simple user interface using Streamlit where users can input a movie they like and receive recommendations.
- Display the recommended movies along with relevant information such as titles, genres, and plot summaries.

## Example

Suppose a user inputs the movie "Inception". The recommender system will:

1. Extract the features of "Inception".
2. Calculate the cosine similarity between "Inception" and all other movies in the dataset.
3. Rank the movies based on their similarity scores.
4. Recommend the top 5 movies that are most similar to "Inception".

## Tools and Technologies

- **Programming Language**: Python
- **Libraries**:
  - `pandas`: For data manipulation and analysis.
  - `scikit-learn`: For vectorization and similarity calculation.
  - `numpy`: For numerical computations.
  - `nltk`: For natural language processing tasks.
  - `Streamlit`: For building the web interface.

## Installation

To run the Movie Mate project locally, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/abhiramathmika/Movie-Mate.git
    cd Movie-Mate
    ```

2. **Install the required packages**:
    ```bash
    pip install pandas scikit-learn numpy nltk streamlit
    ```

3. **Download the dataset** from [TMDB Movie Metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) and place it in the project directory.

4. **Run the Streamlit application**:
    ```bash
    streamlit run app.py
    ```

5. **Access the application**: Open your web browser and go to `http://localhost:8501`.

## Contributing

Contributions are welcome! To contribute to Movie Mate:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For any questions or feedback, please reach out to us at [mirzarafiqahmedc1@gmail.com].
