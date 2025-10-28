# 🎬 Movie Recommendation System  

A content-based movie recommendation system that suggests similar movies based on user input using NLP and cosine similarity.

---

## Overview  
This project is an end-to-end **Machine Learning + Streamlit** application that recommends movies similar to the one selected by the user.  
It uses **text-based features** such as movie overview, genres, keywords, cast, and crew to compute similarity scores between movies and provide recommendations.  
The project demonstrates how data preprocessing, feature engineering, and web app deployment come together in a real-world scenario.

---

## Problem Statement  
With thousands of movies released every year, users struggle to find content they’ll actually enjoy.  
The goal of this project is to build an intelligent system that recommends movies similar to a chosen title — helping users discover new content based on their preferences.

---

## Dataset  
- **Source:** [TMDB 5000 Movies & Credits Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)  
- **Files Used:**  
  - `tmdb_5000_movies.csv`  
  - `tmdb_5000_credits.csv`  
- **Dataset Size:** ~5000 movies  
- **Key Features Used:** `title`, `overview`, `genres`, `keywords`, `cast`, `crew`

---

## Tools and Technologies  

| Category | Tools |
|-----------|--------|
| Language | Python |
| Libraries | pandas, numpy, pickle, requests, pickle, time |
| Framework | Streamlit |
| API Used | TMDB API (for movie posters) |
| IDEs | Jupyter Notebook (Model Building), PyCharm (Frontend App) |

---

## Methods  

### 1. Data Cleaning & Merging  
- Combined movie and credits datasets using the title column.  
- Removed unnecessary columns and handled missing values.  

### 2. Feature Engineering  
- Extracted important text features (overview, genres, keywords, cast, crew).  
- Converted JSON-like data to Python lists using `ast.literal_eval()`.  
- Merged all features into a single text field called `tags`.

### 3. Text Processing  
- Converted all text to lowercase.  
- Removed stop words and extra spaces.  

### 4. Vectorization & Similarity  
- Used `CountVectorizer` to convert text into numerical vectors (bag-of-words).  
- Calculated cosine similarity between all movies to find the most similar ones.

### 5. Model Exporting  
- Saved processed data (`movie_dict.pkl`) and similarity matrix (`similarity.pkl`) using Pickle for reuse.

### 6. Frontend (Streamlit App)  
- Built an interactive UI where users can select a movie.  
- Displayed top 5 similar movies with posters fetched via TMDB API.

---

## 💡 Key Insights  
- Combining textual features like genres, cast, and overview significantly improves similarity accuracy.  
- Stemming reduces redundancy by grouping words with similar roots (e.g., "love", "loves", "loving").  
- Cosine similarity efficiently identifies close relationships even in large datasets.  

---

## Author and Contact
**Author:** Ishant Katiyar  
**Email:** ishantkatiyar68@gmail.com 
**Linkedin:** https://www.linkedin.com/in/ishantkatiyar/
