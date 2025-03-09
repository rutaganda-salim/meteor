# Meteor MQTT Weather Station

This project collects temperature and humidity data from an MQTT broker, saves it in an SQLite database, and displays it with real-time updates and 5-minute averages.

## Features

- 🌡️ Real-time monitoring of temperature and humidity
- 📊 Interactive charts showing 5-minute averages
- 💾 Storage of historical data in an SQLite database
- 📱 Responsive design for both desktop and mobile

## Setup Instructions

### Prerequisites

- Node.js
- npm

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/meteor
   cd meteor
   ```

2. Install the required dependencies:

   ```bash
   npm install
   ```

3. Create a `public` directory and place the `index.html` file inside it:

   ```bash
   mkdir -p public
   cp index.html public/
   ```

4. Start the server:

   ```bash
   npm start
   ```

5. Open your browser and go to `http://localhost:3000` to access the application.

## Project Structure

```
meteor-mqtt-weather-station/
├── public/
│   └── index.html       # Frontend interface with Chart.js visualization
├── server.js            # Express backend with API endpoints and SQLite logic
├── package.json         # Node.js dependencies
├── weather_data.db      # SQLite database (created automatically)
└── README.md            # Setup instructions
```

## How It Works

1. The frontend connects to the MQTT broker and shows real-time temperature and humidity data.
2. Each MQTT message is sent to the backend and saved in the SQLite database.
3. Every 5 minutes, the backend calculates averages and stores them in a separate table.
4. The chart displays up to one hour of historical data (twelve 5-minute intervals).

## Running the Application

1. Go to the project directory.
2. Start the server:
   ```bash
   node server.js
   ```
3. Open your browser and go to `http://localhost:3000`.
