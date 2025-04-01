# Spotify Genre Classification Model

## Overview
This project is a machine learning model that classifies songs into genres based on their features. It uses a **Random Forest Classifier** trained on a Spotify dataset. The model has been deployed as a Flask web application and can be run in a **Docker container**.

## Features
- **Predicts genre** of a song based on its attributes
- **Trained using a Random Forest Classifier** with 95% accuracy
- **Dataset from Spotify**
- **Deployed using Flask & Docker**
- **Can be hosted on AWS Lambda**

## Project Structure
```
Spotify-Genre-Model/
├── app.py                  # Flask API
├── Dockerfile              # Docker setup
├── requirements.txt        # Python dependencies
├── random_forest_model.pkl # Trained model
├── dataset/
│   ├── spotify_dataset.csv # Dataset used for training
├── README.md               # Project documentation
```

## Dataset
- The dataset is sourced from **Spotify** and contains features such as:
  - **Danceability, Energy, Acousticness, Tempo, Speechiness, Valence, etc.**
- The dataset is stored in the `dataset/spotify_dataset.xlsx` file within the project directory.

## Installation & Setup
### Prerequisites
- Python 3.8+
- Flask
- Docker
- Git

### Clone the Repository
```sh
git clone https://github.com/<your-username>/Spotify-Genre-Model.git
cd Spotify-Genre-Model
```

### Install Dependencies
```sh
pip install -r requirements.txt
```

## Running the Model
### 1. Run Flask App Locally
```sh
python app.py
```
- Open **http://127.0.0.1:5000** in your browser.

### 2. Run Using Docker
```sh
docker build -t spotify-model-app .
docker run -d -p 5000:5000 spotify-model-app
```
- Access the app at **http://localhost:5000**

## Deployment on AWS Lambda
- Convert the model into a **Lambda-compatible package**
- Deploy using **Amazon API Gateway**

## Accuracy & Model Evaluation
- **Accuracy:** 95%
- **Confusion Matrix:**
  ```
  [[ 786   12   10   16]
   [  16 3062  164   18]
   [  12  159 4008   31]
   [   5   14   67 1469]]
  ```
- **Classification Report:**
  ```
              precision    recall  f1-score   support
           0       0.96      0.95      0.96       824
           1       0.94      0.94      0.94      3260
           2       0.94      0.95      0.95      4210
           3       0.96      0.94      0.95      1555
  ```

## Author
- Sraddha Varanasi
- GitHub: [Your GitHub Profile](https://github.com/Sraddhavaranasi)


