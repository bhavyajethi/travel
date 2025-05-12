# AI-Powered Music Recommendation System - Proof of Concept

## Objective
This project develops an AI-powered feature for personalized music recommendations based on song audio features, as part of the "AI Assignment_M25". It uses K-Means clustering and cosine similarity to suggest acoustically similar songs.

## Use Case
Smart Recommendation System (Content-Based Music Recommendation)

## Methodology
1.  **Data Loading & Preprocessing**: A dataset of 5000 songs with audio features is loaded and standardized.
2.  **Feature Selection**: Key audio features like `valence`, `danceability`, `energy`, etc., are used.
3.  **Clustering**: K-Means clustering (k=5, determined by Elbow Method) groups similar songs.
4.  **Recommendation**: Cosine similarity within clusters identifies top N recommendations for a given song.

## Code and Files
* `data/data.csv`: The dataset used for this project. https://www.kaggle.com/datasets/vatsalmavani/spotify-dataset
* `notebooks/main.ipynb`: Jupyter notebook containing all the code for data loading, preprocessing, model training, and recommendation generation.
* `images/`: Contains visualizations like the Elbow Method plot and PCA cluster plot.

## Setup and Execution
1.  Clone the repository:
    ```bash
    git clone https://github.com/bhavyajethi/travel
    cd music-recommendation-poc
    ```
2.  Ensure you have Python 3 and the following libraries installed:
    ```bash
    pip install pandas scikit-learn matplotlib flask
    ```
3.  Place the `data.csv` file in the `data/` directory.
4.  Open and run the `notebooks/main.ipynb` Jupyter notebook.
5.  Download the dataset first and run the jupyter notebook.
6.  Run the flask app from the terminal using flask run.

## Key Components (from `main.ipynb`)
* **Data Loading**: Loads and samples the Spotify dataset.
* **Feature Scaling**: Standardizes numerical features.
* **Elbow Method Plot**: Determines the optimal 'k' for K-Means.
* **K-Means Clustering**: Applies K-Means with k=5.
* **PCA Visualization**: Visualizes the formed clusters.
* **Recommendation Function (`recommend_songs`)**: Takes a song name and returns N similar songs.

