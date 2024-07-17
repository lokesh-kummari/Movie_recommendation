# Movie Recommender System

This project is a Movie Recommender System built with Flask. The application allows users to select a movie and receive recommendations for similar movies using a content-based filtering approach.

## Table of Contents

- [Introduction](#introduction)
- [Demo](#demo)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [License](#license)

## Introduction

### Recommender Systems:
1. User Based Recommender Systems
2. Item Based Recommender Systems

### What is a Recommender System?
- Based on previous (past) behaviors, it predicts the likelihood that a user would prefer an item.
- For example, Netflix uses recommendation systems. It suggests people new movies according to their past activities such as watching and voting on movies.
- The purpose of recommender systems is recommending new things that are not seen before by people.

### User Based Collaborative Filtering
- Collaborative filtering makes recommendations according to a combination of your experience and the experiences of other people.
- Steps:
  1. Create a user vs item matrix where each row is a user and each column is an item (like movies, products, or websites).
  2. Compute similarity scores between users.
     - Each row represents users, and each row is a vector.
     - Compute similarity of these rows (users).
  3. Find users who are similar to you based on past behaviors.
  4. Suggest items that you have not experienced before.
- Example:
  - Think that there are two people.
  - The first one watched two movies: "The Lord of the Rings" and "The Hobbit".
  - The second one watched only "The Lord of the Rings".
  - User-based collaborative filtering computes the similarity of these two people and sees both watched "The Lord of the Rings".
  - Then it recommends "The Hobbit" movie to the second one.
  - ![Example](https://preview.ibb.co/feq3EJ/resim_a.jpg)
- Problems:
  - In this system, each row of the matrix is a user. Therefore, comparing and finding similarities between them is computationally hard and requires significant computational power.
  - Habits of people can change over time, making it challenging to make correct and useful recommendations consistently.

## Demo

### Home Page
![Home Page](movie_recommender\screenshots\home.png)

### Recommendations
![Recommendations](movie_recommender\screenshots\rec.png)

## Features

- Select a movie and get recommendations for similar movies.
- Displays movie posters and overviews for recommended movies.
- Simple and clean user interface.

## Installation

### Prerequisites

- Python 3.x
- Flask
- Scikit-learn
- Pandas
- NLTK

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/lokesh-kummari/Movie_recommendation.git
   cd Movie_recommendation
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate
3. Install required packages:
    ```bash
    pip install -r requirements.txt
    ```
4. Download NLTK data:
    import nltk
    nltk.download('punkt')
    nltk.download('stopwords')
5. Place the movie_list.pkl and tfidf_matrix.pkl files in the project directory.
6. Run the Flask app:
    python app.py
7. Open your web browser and go to http://127.0.0.1:5000.

## Usage
Type and choose a movie from the dropdown list.
Click on the "Show Recommendation" button.
The app will display the selected movie's poster and a list of recommended movies with their posters and overviews.

movie-recommender-system/
│
├── screenshots/
│   ├── home.png
│   └── rec.png
│
├── templates/
│   └── index.html
├── app.py
├── movie_list.pkl
├── tfidf_matrix.pkl
├── requirements.txt
└── README.md
## app.py
   This is the main Flask application file that contains the logic for loading data, handling requests, and rendering templates.

## templates/index.html
    This is the HTML template used for rendering the web page.

## movie_list.pkl
    A pickled file containing the movie list data.

## tfidf_matrix.pkl
    A pickled file containing the TF-IDF matrix for the movie descriptions.

## requirements.txt
    A file containing the list of dependencies needed to run the application.

## Dependencies
    Flask
    Scikit-learn
    Pandas
    NLTK
## License
    This project is licensed under the MIT License. See the LICENSE file for details. 

