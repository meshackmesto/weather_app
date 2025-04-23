# SICCO WEATHER APP

📋Overview
Weather App is a responsive web application that provides real-time weather information and forecasts for locations worldwide. Built with Flask (backend) and React (frontend), it delivers a clean, intuitive interface with dynamic backgrounds that change based on current weather conditions.
✨ Features

Current Weather Data: Temperature, humidity, wind speed, pressure, and more
Multi-Day Forecast: Extended 3-day weather outlook
Responsive Design: Optimized for all device sizes from mobile to desktop
Geolocation: Automatically detects user's location for instant weather updates
Dynamic Backgrounds: Visuals change based on weather conditions (sunny, cloudy, rainy, etc.)
Interactive Weather Map: Visual representation of weather patterns
Dark/Light Mode: Toggle between themes for comfortable viewing
Search Functionality: Look up weather for any city worldwide
Weather Alerts: Important weather warnings and advisories
Data Visualization: Charts showing temperature trends and other metrics
Unit Conversion: Switch between metric and imperial units

🛠️ Technology Stack
Backend

Flask: Python web framework
Flask-CORS: Cross-Origin Resource Sharing support
Requests: HTTP library for API calls
Python-dotenv: Environment variable management
OpenWeatherMap API: Weather data source

Frontend

React: UI library
React Router: Navigation and routing
Context API: State management
Axios: HTTP client
Tailwind CSS: Utility-first CSS framework
Chart.js: Data visualization
React-Icons: Icon library
Framer Motion: Animations

📁 Project Structure
weather-app/
├── README.md
├── .gitignore
├── backend/
│   ├── app.py              # Main Flask application
│   ├── config.py           # Configuration settings
│   ├── requirements.txt    # Python dependencies
│   ├── .env.example        # Example environment variables
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── weather.py      # Weather API utility functions
│   │   └── validators.py   # Input validation
│   └── tests/
│       ├── __init__.py
│       └── test_api.py     # API tests
└── frontend/
    ├── public/
    │   ├── index.html
    │   └── assets/
    │       └── images/     # Static images
    ├── src/
    │   ├── index.js        # Entry point
    │   ├── App.js          # Main component
    │   ├── api/            # API integration
    │   ├── components/     # React components
    │   ├── context/        # Context providers
    │   ├── hooks/          # Custom hooks
    │   ├── pages/          # Page components
    │   ├── styles/         # CSS and styling
    │   └── utils/          # Utility functions
    ├── package.json        # NPM dependencies
    └── tailwind.config.js  # Tailwind configuration
🚀 Getting Started
Prerequisites

Node.js (v14+)
npm or yarn
Python (v3.8+)
OpenWeatherMap API key (free tier available)

Backend Setup

Navigate to the backend directory:
bashcd weather-app/backend

Create and activate a virtual environment:
bash# Create virtual environment
python -m venv venv

# Activate on Windows
venv\Scripts\activate

# Activate on macOS/Linux
source venv/bin/activate

Install dependencies:
bashpip install -r requirements.txt

Create a .env file from the example:
bashcp .env.example .env

Add your OpenWeatherMap API key to the .env file:
WEATHER_API_KEY=your_api_key_here
FLASK_APP=app.py
FLASK_ENV=development

Run the Flask server:
bashpython app.py
The backend should now be running at http://localhost:5000

Frontend Setup

Navigate to the frontend directory:
bashcd weather-app/frontend

Install dependencies:
bashnpm install
# or
yarn install

Start the development server:
bashnpm start
# or
yarn start
The frontend should now be running at http://localhost:3000

🌐 API Endpoints
Weather Data
GET /api/weather?location={city_name}
GET /api/weather?lat={latitude}&lon={longitude}
Forecast Data
GET /api/forecast?location={city_name}&days={number_of_days}
GET /api/forecast?lat={latitude}&lon={longitude}&days={number_of_days}
Test Endpoint
GET /api/test