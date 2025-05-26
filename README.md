# 🎬 Movie Recommender System (TMDB Dataset)

A **Content-Based Movie Recommender System** built using the TMDB dataset and powered by **Cosine Similarity**. This project suggests movies based on user preferences such as genre, keywords, cast, crew, and overview, helping users discover new titles similar to the ones they like.

## 📌 Features

- ✅ Content-Based Filtering using movie metadata
- ✅ Cosine Similarity for finding similar movies
- ✅ TMDB dataset integration (movies, credits, keywords)
- ✅ Clean and interactive UI with Streamlit (optional)
- ✅ Search and recommend functionality
- ✅ Poster fetching using TMDB API

---

## 🗂️ Dataset Used

We use the **TMDB 5000 Movie Dataset**, which includes:
- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

You can find the dataset on [Kaggle](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata).

---

## 🧠 Approach

1. **Data Preprocessing**:
   - Merge `movies` and `credits` datasets.
   - Extract and clean features like `genres`, `keywords`, `cast`, `crew`, and `overview`.
   - Create a new feature called `tags` by combining relevant textual metadata.

2. **Vectorization**:
   - Convert tags into lowercase and remove stopwords.
   - Apply **CountVectorizer** to convert text into numerical vectors.
   - Calculate **cosine similarity** between vectors to find similar movies.

3. **Recommendation Logic**:
   - Based on cosine similarity scores, return top N similar movies.

---

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/movie-recommender-system-tmdb-dataset.git
cd movie-recommender-system-tmdb-dataset
```

### 2. Install Dependencies
Make sure you have Python 3.7+ installed.

```bash
pip install -r requirements.txt
```

### 3. Run the App (Optional: Streamlit UI)
```bash
streamlit run app.py
```

---

## 🔍 How It Works

```python
# Example usage
recommend('Avatar')
```

**Output:**
```
- John Carter
- Guardians of the Galaxy
- Pacific Rim
- The Avengers
- The Fifth Element
```

---

## 📦 File Structure

```
movie-recommender-system-tmdb-dataset/
│
├── data/
│   ├── tmdb_5000_movies.csv
│   └── tmdb_5000_credits.csv
│
├── app.py                # Streamlit App (Optional)
├── recommender.py        # Core recommendation logic
├── utils.py              # Data cleaning and helper functions
├── requirements.txt
└── README.md
```

---

## 🧪 Technologies Used

- Python
- Pandas & NumPy
- Scikit-learn (CountVectorizer, Cosine Similarity)
- NLTK (Natural Language Processing)
- Streamlit (Web UI)
- TMDB API (for posters)

---

## 📷 Screenshots

| Input Movie | Recommended Movies |
|-------------|--------------------|
| Inception   | The Prestige, Interstellar, Shutter Island, etc. |
| Iron Man    | Iron Man 2, Avengers, Captain America, etc.      |

---

## 📈 Future Improvements

- Add **collaborative filtering** or hybrid approach.
- Use **TF-IDF** or **Word2Vec/BERT** embeddings.
- Deploy on **Render/Heroku** or as a **Flask web app**.
- Add **user login & history tracking**.

---

## 🧑‍💻 Author

- **Shashikant Kumar Bind**  
- [LinkedIn](https://linkedin.com/in/shashikantkumarbind)  
- [GitHub](https://github.com/stechbindra2)

---

## ⭐️ Show Your Support

If you like this project, consider giving it a ⭐️ on GitHub!

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.