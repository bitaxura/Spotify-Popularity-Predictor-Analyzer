# Spotify Song Popularity Predictor

Predict the popularity of Spotify tracks using machine learning, and analyze how musical trends have changed over time.

---

## Overview
This project explores the relationship between audio features (like danceability, energy, and valence) and song popularity on Spotify.  
It uses datasets from **Kaggle** (Spotify audio features) combined with **live data from the Spotify Web API** to:
- Train a model to predict track popularity.
- Analyze which song attributes most influence popularity.
- Compare musical trends between **2020** and **2023**.

---

## Motivation
As streaming dominates the music industry, understanding what makes a song popular has real-world applications — from music marketing to personalized recommendations.  
This project applies **data science and machine learning** to uncover these insights and build a **predictive model** based on measurable musical features.

---

## Features
- **Exploratory Data Analysis (EDA)** — visualize correlations between features like energy, danceability, and popularity.  
- **Popularity Prediction Model** — trained with Random Forest Regression on cleaned Spotify datasets.  
- **Temporal Trend Analysis** — compare feature importance and popularity distribution between years (e.g., 2020 vs 2023).  
- **Spotify API Integration** — update and validate real-time song metrics using [Spotipy](https://spotipy.readthedocs.io/).  

---

## Project Structure
```

Spotify-Popularity-Predictor/
│
├── data/
│   ├── spotify_2020.csv
│   ├── spotify_2023.csv
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_model_training.ipynb
│   └── 04_trend_analysis.ipynb
│
├── src/
│   ├── utils.py
│   ├── spotify_api.py
│   └── modeling.py
│
├── requirements.txt
└── README.md

````

---

## Tech Stack
- **Languages:** Python 3.10+
- **Libraries:** Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib, Spotipy
- **Model:** Random Forest Regressor (with feature importance visualization)
- **Data Sources:**
  - [Spotify Tracks Dataset (Kaggle)](https://www.kaggle.com/datasets)
  - Spotify Web API (via Spotipy)

---

## Setup & Usage

### Clone this repo
```bash
git clone https://github.com/yourusername/Spotify-Popularity-Predictor.git
cd Spotify-Popularity-Predictor
````

### Install dependencies

```bash
pip install -r requirements.txt
```

### Set up Spotify API credentials

Create a `.env` file with your credentials:

```
SPOTIPY_CLIENT_ID=your_client_id
SPOTIPY_CLIENT_SECRET=your_client_secret
```

### Run the notebooks

Start Jupyter and explore step by step:

```bash
jupyter notebook notebooks/
```

---

## Results

* Model achieved an **R² score of ~0.50** on unseen data.
* **Danceability**, **energy**, and **valence** were top predictors of popularity.
* Observed that songs post-2020 are generally **shorter** and **higher energy**, aligning with modern pop trends.

---

## Next Steps

* Add neural network model for comparison,
* Perform genre-specific modeling.
* Build a Streamlit dashboard for interactive feature exploration.


## License

This project is licensed under the MIT License, see the [LICENSE](LICENSE) file for details.