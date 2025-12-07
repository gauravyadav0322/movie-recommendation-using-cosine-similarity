# Movie Recommendation System Using Cosine Similarity

This repository implements a content-based movie recommendation system using cosine similarity on movie metadata (genre, cast, director, etc.).  
It helps users find movies similar to a given movie based on features rather than user ratings.  

## Table of Contents

- Overview  
- Features  
- Dataset  
- Methodology  
- Project Structure  
- Installation  
- Usage  
- Results / Output  
- Future Improvements  
- License  

## Overview

The goal of this project is to demonstrate how a simple, content-based recommendation engine works. By converting movie metadata into a combined “feature vector” and using cosine similarity, the system returns movies that are closest in “feature space” to a user-selected movie.  

## Features

- Content-based recommendation using metadata (genre, cast, director, etc.).  
- Cosine similarity calculation among movie feature vectors.  
- Works on a dataset of Bollywood / other movies (or a dataset you supply).  
- Easy to run via a Jupyter Notebook for demonstration.  

## Dataset

- The main dataset file: `bollywood1to950.csv` (or whichever file you use).  
- Contains metadata such as movie title, actors, director, genres, plot / description (if available).  

## Methodology

1. Load and clean the dataset.  
2. Extract relevant metadata fields (e.g. title, genre, cast, director).  
3. Combine these fields into a single “feature string” per movie.  
4. Vectorize the feature strings using a vectorizer (CountVectorizer or TF-IDF).  
5. Compute pairwise cosine similarity between all movie vectors.  
6. For a given input movie, output the top N most similar movies based on similarity score.  

## Project Structure

/ ← root
├── data/ ← (optional) folder for dataset
├── bollywood1to950.csv ← main dataset (or as applicable)
├── Recommending Movies Using Cosine Similarity.ipynb ← main Jupyter notebook
├── requirements.txt ← dependencies (if any)
└── README.md ← this file
