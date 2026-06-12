# 📚 Book Recommender System
 
A machine learning-powered book recommendation system that suggests **5 similar books** based on your selection — complete with cover images. Built using **collaborative filtering** with K-Nearest Neighbors (KNN) and deployed as an interactive Streamlit web app.

---
 
## 🚀 Live Demo
 
🔗 **[Try it here - book-recommender-ml-ravi.streamlit.app](https://book-recommender-ml-ravi.streamlit.app/)**
 
---
 
## 🧠 How It Works
 
This system uses **Memory-Based Collaborative Filtering** — the same core idea behind recommendation engines at Amazon and Goodreads.
 
1. **User-Book Pivot Matrix** — A matrix is constructed from user ratings data, where rows represent books and columns represent users. Each cell holds the rating a user gave to a book.
2. **KNN Similarity** — A K-Nearest Neighbors model finds the `n` books that are closest in the rating space to the selected book, using cosine similarity.
3. **Poster Fetching** — The app dynamically fetches book cover images from the dataset's image URLs to display alongside each recommendation.
4. **Streamlit UI** — A clean dropdown lets you select any book and instantly see 5 personalized recommendations with their covers.
---
 
## 🛠️ Tech Stack
 
| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas & NumPy | Data processing |
| Scikit-learn | KNN model |
| Pickle | Model & artifact serialization |
| Streamlit | Web app deployment |
 
---
 
## 📁 Project Structure
 
```
Book_Recommender_System/
│
├── artifacts/
│   ├── model.pkl            # Trained KNN model
│   ├── book_names.pkl       # List of all book titles
│   ├── book_pivot.pkl       # User-book pivot matrix
│   └── final_ratings.pkl    # Book metadata with image URLs
│
├── data/                    # Raw dataset
├── src/                     # Source modules
├── app.py                   # Streamlit application
├── book_recommender_notes.ipynb  # EDA & model building notebook
├── requirements.txt
└── README.md
```
 
---
 
## ⚙️ Run Locally
 
```bash
# 1. Clone the repository
git clone https://github.com/RaviNamdeoo/Book_Recommender_System.git
cd Book_Recommender_System
 
# 2. Install dependencies
pip install -r requirements.txt
 
# 3. Launch the app
streamlit run app.py
```
 
---
 
## 📊 Dataset
 
The project uses the **Book-Crossing Dataset**, which contains:
- ~270,000 books
- ~1.1 million ratings from ~278,000 users
Only books with a minimum number of ratings were kept to ensure meaningful recommendations (popularity filtering).
> NOTE that afew Books dont have any Images or are expired so they are unable to be seen 
 
---
 
## 🔑 Key Concepts
 
- **Collaborative Filtering** — Recommends books based on patterns in user ratings, without needing book content/metadata
- **User-Book Pivot Matrix** — Sparse matrix representing user-book interactions
- **KNN (n_neighbors=6)** — Finds the 6 nearest neighbors; the queried book is excluded, returning 5 recommendations
- **Cosine Similarity** — Measures the angle between book vectors in rating space to determine closeness
---
 
## 👤 Author
 
**Ravi Namdeo**
- GitHub: [@RaviNamdeoo](https://github.com/RaviNamdeoo)
- LinkedIn: [RaviNamdeo](https://www.linkedin.com/in/ravinamdeo)
