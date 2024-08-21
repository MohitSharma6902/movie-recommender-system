# Movie Recommender System

## Overview

This project is a Movie Recommender System built using Python. It utilizes a content-based recommendation approach to suggest movies similar to the one selected by the user. The system leverages a pre-trained movie recommendation model and retrieves movie posters from The Movie Database (TMDb) API to display recommendations.

## Features

- **Movie Recommendation**: Based on the selected movie, the system recommends similar movies using a precomputed similarity matrix.
- **Poster Display**: Fetches and displays movie posters for recommended movies.
- **Interactive UI**: Built using Streamlit for an easy-to-use web interface.

## Requirements

To run this project, you need to have the following Python packages installed:

- `pickle`
- `streamlit`
- `requests`

You can install the required packages using pip:

```bash
pip install streamlit requests
```

## Setup

1. **Clone the Repository**: 

   ```bash
   git clone https://github.com/yourusername/movie-recommender.git
   cd movie-recommender
   ```

2. **Download Data Files**: Ensure you have the `movie_list.pkl` and `similarity.pkl` files. Place these files in the `model` directory of the project.

3. **API Key**: You will need an API key from The Movie Database (TMDb) to fetch movie posters. Replace `YOUR_API_KEY` in the `fetch_poster` function with your actual API key.

   ```python
   url = "https://api.themoviedb.org/3/movie/{}?api_key=YOUR_API_KEY&language=en-US".format(movie_id)
   ```

## Running the App

1. **Start Streamlit**:

   Navigate to the project directory and run the following command:

   ```bash
   streamlit run app.py
   ```

   This will start a local server and open the app in your default web browser.

2. **Use the App**:

   - Select a movie from the dropdown menu.
   - Click the "Show Recommendation" button to view similar movie recommendations along with their posters.

## Code Overview

- **fetch_poster(movie_id)**: Fetches the movie poster from TMDb using the provided movie ID.
- **recommend(movie)**: Computes recommendations based on the similarity matrix and retrieves corresponding movie posters.
- **Streamlit UI**: Displays the movie selection dropdown, recommendation button, and results in a web interface.

## Troubleshooting

- **API Errors**: Ensure your TMDb API key is correct and that the service is available.
- **File Errors**: Verify that `movie_list.pkl` and `similarity.pkl` are in the correct directory.

## Contributing

Feel free to fork the repository and submit pull requests. For any issues or suggestions, open an issue on GitHub.

