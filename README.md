# Weather MCP Server

This repository contains the implementation of a Weather MCP (Model Context Protocol) Server. The server provides weather information for a given city using the Open-Meteo API.

## Features

- Fetches weather data for any city.
- Provides current temperature, relative humidity, apparent temperature, precipitation, and weather code.
- Built using the Model Context Protocol SDK.

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd mcp-weather-server
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Usage

1. Start the server:
   ```bash
   npm start
   ```

2. Use the `get-weather` tool to fetch weather data for a city. Example:
   ```bash
   get-weather "London"
   ```

## Project Structure

- `main.ts`: The main entry point of the server.
- `package.json`: Contains project metadata and dependencies.

## API Details

The server uses the following APIs:

1. **Geocoding API** (Open-Meteo):
   - Endpoint: `https://geocoding-api.open-meteo.com/v1/search`
   - Purpose: Fetches latitude and longitude for a given city.

2. **Weather API** (Open-Meteo):
   - Endpoint: `https://api.open-meteo.com/v1/forecast`
   - Purpose: Fetches weather data using latitude and longitude.

## Error Handling

- If the city is not found, the server returns a message indicating the issue.
- If there is an error fetching weather data, the server returns the error message.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
