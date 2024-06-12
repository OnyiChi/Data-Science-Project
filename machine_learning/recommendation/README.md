# Movie Recommendation System

The Movie Recommendation System is a Python-based application designed to suggest movies similar to the user's input. It utilizes a dataset containing movie information such as genres, keywords, cast, and director to compute the similarity between movies. The system employs the TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer to convert text data into feature vectors and then calculates the cosine similarity between movies based on these vectors.

## Usage

1. **Importing Dependencies:** The system imports necessary libraries including NumPy, pandas, and scikit-learn for data manipulation and cosine similarity calculation.

You can install these libraries using pip:
```
pip install numpy pandas matplotlib seaborn scikit-learn
```

3. **Data Collection and Pre-Processing:** The dataset used in this project is `movies.csv`, which contains information about various movies, including their genres, keywords, cast, and directors. The data preprocessing steps involve loading the dataset, handling missing values, and combining relevant features.
Missing values in these features are replaced with empty strings, and the selected features are combined into a single string representation for each movie. Text data is then converted into feature vectors using TF-IDF vectorization.

6. **Cosine Similarity:** Cosine similarity is calculated between all pairs of movies based on their feature vectors. This similarity metric quantifies the similarity between movies' textual descriptions.

7. **Movie Recommendation:** Upon receiving a movie name input from the user, the system finds the closest match to the input movie name from the dataset. It then identifies similar movies based on the cosine similarity scores and presents a list of recommended movies to the user.

## Example Usage

```python
Enter Movie Name : iron man
```

Movies suggested for you:
- Iron Man
- Iron Man 2
- Iron Man 3
- Avengers: Age of Ultron
- The Avengers
- Captain America: Civil War
- Captain America: The Winter Soldier
- Ant-Man
- X-Men
- Made
