# 🎬 Movie Recommender System

This project is a simple **content-based movie recommender system** built using Python. It loads a dataset of movies, performs preprocessing and data cleaning, and then recommends movies based on similarity.

## 🛠️ Technologies Used

- Python  
- NumPy  
- Pandas  

## 📊 Dataset & Cleaning

We begin by importing a movie dataset. Several preprocessing steps are applied:

- **Numeric conversion**: The following columns were converted to numeric types to enable similarity computations:
  - `Meta_score`
  - `IMDB_Rating`
  - `Runtime`
  - `Gross`
  - `Votes`
  
- **Missing data handling**:
  - Rows with only a **few missing values** (e.g., in `Meta_score` or `Gross`) were **dropped** to ensure data consistency.

## 💡 Recommender System Logic

A simple recommendation engine is implemented:

1. The user inputs the name of a movie.
2. The system finds **5 most similar movies** using **dot product (inner product)** similarity.
3. We use:
   - A **NumPy matrix** to store numerical features of the movies.
   - A **Pandas DataFrame** to map the similarity scores and movie titles.
   - **`np.dot()`** to calculate similarity between movies.

## 🧪 Example

If a user inputs `"The Godfather"`, the system returns 5 similar movies based on feature similarity.

## 🚀 Run the Project

1. Clone the repository.
2. Run the Jupyter Notebook (`DA-03.ipynb`).
3. Input a movie name when prompted.
4. Get your top 5 recommendations!

---

Feel free to modify the thresholds for missing data handling or the number of recommended movies.
