# 🎬 Movie Recommender System

A Content-Based Movie Recommendation System built using Python and Streamlit.  
This system recommends 5 similar movies based on the movie selected by the user.

---

## 🧠 How the Project Works

### 1️⃣ Data Preprocessing
The movie dataset was cleaned and important features such as:
- Genres  
- Keywords  
- Cast  
- Crew  

were combined to create a single text representation for each movie.

**Why?**  
In content-based filtering, recommendations are made by comparing movie content instead of user ratings.

---

### 2️⃣ Feature Engineering
Text data was converted into numerical format using:

- Count Vectorization  

**Why?**  
Machine learning models cannot understand text directly, so we convert textual data into numerical vectors.

---

### 3️⃣ Similarity Calculation
We calculated similarity between movies using:

- Cosine Similarity  

This created a similarity matrix (`similarity.pkl`) where every movie is compared with every other movie.

**Why?**  
Cosine similarity measures how similar two movies are based on their content features.

---

### 4️⃣ Recommendation Logic
When a user selects a movie:

1. The system finds the movie index  
2. Retrieves similarity scores from the similarity matrix  
3. Sorts movies based on highest similarity  
4. Returns the top 5 most similar movies  

---

### 5️⃣ Web Application (Streamlit)
A simple and interactive web interface was built using Streamlit:

- Dropdown to select a movie  
- Button to generate recommendations  
- 5 columns to display recommended movie posters  

---

### 6️⃣ TMDB API Integration
Movie posters are fetched dynamically using the TMDB API.

**Why?**  
To improve user experience and make the application visually interactive.

---

## 🛠️ Technologies Used

- Python  
- Pandas  
- Scikit-learn  
- Streamlit  
- TMDB API  

---

## 📂 Project Structure

- `app.py` → Main Streamlit application  
- `movie_dict.pkl` → Processed movie dataset  
- `similarity.pkl` → Precomputed similarity matrix  

---

