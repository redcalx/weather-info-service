# Weather Info Service

## Overview
The Weather Info Service is a microservice that provides weather information based on city names. It fetches data from an external weather API and serves it through a RESTful interface.

## Project Structure
```
weather-info-service
├── src
│   ├── index.js
│   ├── services
│   │   └── weatherService.js
│   ├── controllers
│   │   └── weatherController.js
│   └── utils
│       └── apiClient.js
├── package.json
├── serverless.yml
├── .env
└── README.md
```

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd weather-info-service
   ```

2. **Install Dependencies**
   Make sure you have Node.js installed. Then run:
   ```bash
   npm install
   ```

3. **Configure Environment Variables**
   Create a `.env` file in the root directory and add your API keys and configuration settings:
   ```
   WEATHER_API_KEY=your_api_key_here
   ```

4. **Run the Service Locally**
   You can start the service locally using:
   ```bash
   npm start
   ```

5. **Deploying to AWS**
   To deploy the service using the Serverless Framework, ensure you have the Serverless CLI installed and configured. Then run:
   ```bash
   serverless deploy
   ```

## Usage
Once the service is running, you can make requests to get weather information. For example:
```
GET /weather?city=London
```

## Contributing
Feel free to submit issues or pull requests if you would like to contribute to the project.

## License
This project is licensed under the MIT License.