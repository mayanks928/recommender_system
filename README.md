# Music Recommender

## Overview

The Spotify Music Recommender, named Music Match, is a Streamlit-based web application designed as the final year project for a Data Science Honors degree. The application leverages Spotify's API and custom machine learning models to recommend music tracks based on user preferences.

Users can input their favorite playlist, song, or artist and receive tailored recommendations through interactive and customizable options.

## Features

### 1. Playlist Recommendations
- Recommends songs from the dataset that share similar audio and track features with the user-provided playlist.
- Utilizes audio features like danceability, energy, and acousticness.

### 2. Song Recommendations
- Suggests songs similar to a user-provided track.
- Uses audio features, track popularity, and release period for recommendation.

### 3. Artist Top Tracks
- Displays an artist's top tracks by region based on Spotify's catalog.

## Models

### 1. **Model 1**
- Focuses on audio features and genre similarity.
- Gives higher importance to genre alignment.

### 2. **Model 2**
- Balances importance across audio features, track popularity, and artist genre.

### 3. **Model 3**
- Provides customizable weights for audio features, track characteristics, and genres.
- Users can adjust the relative importance of these components.

### 4. **Spotify Model**
- Directly fetches recommendations from Spotify's API using a seed track.
- No custom model is involved.

## Inputs

### Playlist
- Input: Spotify Playlist URL.
- Options:
  - Number of genres to prioritize.
  - Limit on recommendations from the same artist.

### Song
- Input: Spotify Song URL.
- Options:
  - Adjust genre importance and feature weights (for Model 3).

### Artist
- Input: Spotify Artist URL.

## Key Components
1. **Track Vectorization:** Each track in the dataset is represented as a vector using features such as genre, tempo, and other musical attributes.
2. **Playlist Vectorization:** Playlists are represented as aggregate vectors derived from their constituent tracks.
3. **Cosine Similarity Calculation:** For a given playlist or set of preferences, the system calculates cosine similarity to rank songs in the dataset for recommendation.
