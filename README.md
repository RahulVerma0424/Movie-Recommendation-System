# 🎬 Movie Recommendation System using Cosine Similarity

## Problem Statement

With thousands of movies released every year, helping users discover movies based on their preferences is essential. This project aims to build a **content-based movie recommender system** using metadata such as genre, director, cast, and keywords. The model uses **cosine similarity** to recommend movies that are similar in content and style.

---

## Dataset Used

- **TMDB 5000 Movie Dataset**
  - `movies.csv` and `credits.csv` merged for complete metadata
- Key features extracted and used:
  - `title`, `overview`, `genres`, `keywords`, `cast`, `crew`

---

## Data Preprocessing & Feature Engineering

- Merged datasets on movie titles
- Extracted and cleaned:
  - Top 3 cast members
  - Director from crew list
  - Genre and keywords
- Removed stopwords and special characters
- Built a **"tags"** feature combining all key text-based fields
- Used **CountVectorizer** to convert tags into feature vectors

---

## Model Building

- Calculated **cosine similarity** between movie vectors
- Created a function `recommend(movie_name)` that:
  - Finds the movie
  - Gets top 5 most similar movies based on cosine similarity scores

---

## Evaluation & Sample Output

- Input: `Avatar`  
- Output Recommendations:
  - Guardians of the Galaxy
  - Star Wars
  - John Carter
  - 2001: A Space Odyssey
  - Star Trek

 System gives human-understandable, genre-specific recommendations.

---

## Conclusion

This project showcases a **content-based filtering approach** for movie recommendation using NLP and vector similarity. While it's simple, it lays the foundation for more advanced hybrid and collaborative filtering systems.

---


## Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas | Data manipulation |
| NumPy | Arrays & vectors |
| NLTK | Text cleaning |
| Scikit-learn | CountVectorizer & Cosine Similarity |
| Jupyter Notebook | Development environment |

---


## How to Run

```bash
1. Clone this repository
2. Open `movie_recommender.ipynb` in Jupyter Notebook
3. Run all cells
4. Call the function `recommend("Movie Name")` to get recommendations
