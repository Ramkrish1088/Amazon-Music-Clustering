# 🎵 Amazon Music Clustering

Automatically cluster Amazon Music songs based on audio features using unsupervised learning. This enables smarter **playlist curation**, **song recommendations**, and **artist/market insights**.

---

## 📌 Project Overview

With millions of tracks available, manually organizing songs by genre or mood is inefficient. This project uses **K-Means** and **DBSCAN** clustering on features like `danceability`, `energy`, `valence`, and more to group similar songs based on how they **sound**.

---

## 🎯 Key Goals

- ✅ Automatically generate meaningful song clusters  
- ✅ Visualize clusters for easy interpretation  
- ✅ Provide actionable insights for recommendation and analysis  
- ✅ Enable downstream uses like playlist building or artist profiling  

---

## 📂 Dataset

**File:** `single_genre_artists.csv`

### 🔢 Numeric Features:
- `danceability`, `energy`, `loudness`, `speechiness`, `acousticness`,  
  `instrumentalness`, `liveness`, `valence`, `tempo`, `duration_ms`,  
  `popularity_songs`, `followers`, `popularity_artists`

### 🏷️ Reference Columns:
- `track_id`, `track_name`, `artist_name`, `genres`

These features describe a song’s **rhythm**, **mood**, **intensity**, and **instrumentation**.

---

## 🧠 Approach

### 🔧 Data Preprocessing
- Dropped non-relevant columns (IDs, dates, keys, etc.)
- Handled missing values
- Scaled numeric features using `StandardScaler`

### 🔍 Clustering
- Applied **K-Means** with Elbow Method and Silhouette Score
- Applied **DBSCAN** with PCA and k-distance optimization
- Compared models using clustering metrics

### 📊 Evaluation
- **Silhouette Score** to assess cohesion/separation
- Mean feature analysis per cluster (to interpret "mood" or "style")

### 📈 Visualization
- PCA scatterplots (2D)
- Heatmaps and bar plots for cluster characteristics

---

## 📤 Outputs

- ✅ `amazon_music_clusters_all_methods.csv`: Original dataset + cluster labels  
- ✅ Visualizations: PCA plots, heatmaps, feature distribution plots  
- ✅ Jupyter Notebook: Full analysis and clustering pipeline  
- ✅ *(Optional)* Streamlit app for interactive cluster browsing  

---

## 🛠️ Tech Stack

| Tool             | Use                            |
|------------------|---------------------------------|
| `Python`         | Programming language            |
| `Pandas`, `NumPy`| Data processing and analysis    |
| `scikit-learn`   | Clustering, metrics, PCA        |
| `Matplotlib`, `Seaborn` | Visualizations         |
| `Streamlit` *(optional)* | Web app for cluster UI  |





