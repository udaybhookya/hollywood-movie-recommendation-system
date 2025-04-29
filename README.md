# Hollywood Movie Recommendation System

![Python 3.7](https://img.shields.io/badge/python-3.7-red) ![Flask](https://img.shields.io/badge/framework-flask-orange) ![HTML/CSS](https://img.shields.io/badge/frontend-HTML%2FCSS-yellow) ![TMDB API](https://img.shields.io/badge/API-TMDB-lightgrey)

## Overview

An AI-powered, content-based movie recommendation system built with Flask and a responsive HTML/CSS/Bootstrap frontend. Users enter a film title and receive personalized suggestions by comparing feature embeddings (genres, plot keywords, cast metadata) using cosine similarity.

## Key Features

- **Custom Dataset**: Curated and preprocessed Hollywood movie data (20,000+ entries).
- **Content-Based Filtering**: Leverages TF–IDF embeddings and cosine similarity to find similar titles.
- **RESTful API**: Lightweight Flask backend serving recommendation endpoints.
- **Responsive UI**: Clean, Bootstrap-powered interface for seamless user experience.

## Dataset

Download the dataset used to train and test the model:

- [Hollywood Movies (Kaggle)](https://www.kaggle.com/udaychandra/hollywood-movies)
- [IMDb 5000 Movie Dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)
- [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)
- [American Films of 2018](https://en.wikipedia.org/wiki/List_of_American_films_of_2018)
- [American Films of 2019](https://en.wikipedia.org/wiki/List_of_American_films_of_2019)
- [American Films of 2020](https://en.wikipedia.org/wiki/List_of_American_films_of_2020)

## Getting a TMDB API Key

1. Sign up for a free TMDB account and verify your email.
2. Go to **Account Settings > API**.
3. Apply for and copy your API key.

## Installation & Usage

1. Clone this repository.
2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set your TMDB API key in `.env`:
   ```bash
   TMDB_API_KEY=your_api_key_here
   ```
5. Run the Flask server:
   ```bash
   flask run
   ```
6. Open `http://localhost:5000` in your browser.

## How It Works

1. User submits a movie title.
2. Backend fetches metadata from TMDB.
3. Precomputed TF–IDF vectors and cosine similarity scores generate recommendations.
4. Results are returned via JSON and rendered in the frontend.

---

<p align="center">Made with ❤️ and Flask</p>

