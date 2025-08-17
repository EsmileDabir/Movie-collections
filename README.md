🎬 Movie Recommendation System

This is a Movie Recommendation Web App built using Streamlit. It recommends movies similar to the one selected by the user and displays their posters using The Movie Database (TMDb) API.

🚀 Features

Select a movie from the dropdown.

Get Top 10 movie recommendations instantly.

Movie posters are fetched dynamically from TMDb API.

Responsive layout with two rows (5 movies per row).

Handles missing posters gracefully with a placeholder image.

🛠️ Tech Stack

Python

Streamlit (for UI)

Pickle (for loading pre-trained similarity data)

Requests (to fetch posters from TMDb API)

📂 Project Structure
.
├── movie_list.pkl         # Pickled DataFrame of movies with titles & IDs
├── similarity.pkl         # Pickled similarity matrix
├── app.py                 # Main Streamlit app file (your script)
└── README.md              # Project documentation

⚙️ Installation

Clone the repository:

git clone https://github.com/your-username/movie-recommender.git
cd movie-recommender


Create a virtual environment (optional but recommended):

python -m venv venv
source venv/bin/activate     # On Mac/Linux
venv\Scripts\activate        # On Windows


Install dependencies:

pip install -r requirements.txt


Run the app:

streamlit run app.py

📦 Requirements

Create a requirements.txt file with:

streamlit
requests
pandas

🔑 API Key Setup

This project uses TMDb API to fetch posters.
Replace the placeholder key in app.py with your own API key:

url = f"https://api.themoviedb.org/3/movie/{movie_id}?api_key=YOUR_API_KEY&language=en-US"


Get your free API key from: TMDb API

🎯 How It Works

User selects a movie from the dropdown.

The app finds similar movies using the pre-computed similarity matrix (similarity.pkl).

Posters are fetched via TMDb API.

Top 10 recommendations are displayed in a clean 2-row grid layout.
