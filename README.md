# Agriculture Assistance Web Application (Krishi Sahayatha)

## Problem Statement

This web application, "Krishi Sahayatha," aims to address critical issues faced by farmers, including:

1.  **Farmer Suicides:** Providing resources and information to alleviate factors contributing to farmer suicides, such as financial strain, lack of market access, and lack of awareness of support policies.
2.  **Insect Infestation:** Assisting farmers in identifying crop pests and providing information on effective and affordable pest control methods.
3.  **Weather Forecast:** Delivering accurate and localized weather forecasts to help farmers make informed decisions about their crops.
4.  **Equipment Issues:** Providing troubleshooting guides and connecting farmers with local technicians for issues related to electricity supply, motors, and borewells.
5.  **Medicine/Chemical Usage:** Guiding farmers on the correct and safe usage of medicines and chemicals for their crops.
6.  **Rain Prediction:** Helping farmers predict rains based on crop stage.
7.  **Marketing:** Assisting farmers in selling their products, finding storage, and knowing current market rates.
8.  **Farm Implements:** Providing information about farm implements.

The application is designed to work in low-resource settings and supports multiple languages (Hindi, Kannada, Telugu, Tamil).

## Features

* **Multi-language support:** The application supports Hindi, Kannada, Telugu, and Tamil.
* **Farmer Suicide Prevention Resources:** Provides information on government schemes, financial literacy, and mental health support.
* **Pest Detection and Solutions:** Helps farmers identify pests and suggests solutions.
* **Localized Weather Forecasts:** Provides accurate weather information.
* **Equipment Support:** Offers troubleshooting and connects farmers with local technicians.
* **Medicine/Chemical Usage Guidance:** Provides information on safe and effective use of chemicals.
* **Rain Prediction:** Predicts the rain based on crop stages.
* **Marketing Assistance:** Helps farmers sell products, find storage, and get current market rates.
* **Farm Implements Information:** Provides information about implements.

## Technical Architecture

The application follows a full-stack architecture:

* **Frontend:** React.js
* **Backend:** Node.js with Express.js
* **Database:** MongoDB
* **API:** Google Generative AI API (for content generation)
* **Weather API:** OpenWeatherMap (or similar)

## Folder Structure


agriculture-assistance/
├── client/             # Frontend code (React)
│   ├── public/
│   │   ├── index.html  # Main HTML file
│   │   └── assets/     # Images, fonts, etc.
│   ├── src/
│   │   ├── components/ # Reusable React components
│   │   ├── pages/      # Main page components
│   │   ├── styles/     # CSS files
│   │   ├── utils/      # Utility functions (e.g., i18n)
│   │   ├── App.js      # Main application component
│   │   └── index.js    # Entry point for React
│   └── package.json    # Frontend dependencies and scripts
├── server/             # Backend code (Node.js/Express)
│   ├── controllers/    # Logic for handling requests
│   │   ...
│   ├── models/         # Data models (using Mongoose)
│   │   ...
│   ├── routes/         # API routes
│   │   ...
│   ├── config/         # Configuration files
│   │   └── config.json # API keys (Less sensitive data, more sensitive in .env)
│   ├── app.js          # Main Express application
│   └── package.json    # Backend dependencies and scripts
└── README.md         # Project documentation


## API Endpoints

* `GET /api/weather?lat={latitude}&lon={longitude}&lang={language}`: Fetch weather data.
* `POST /api/pest/advice`:  Send description of pest, get advice.
* `GET /api/info/policies?lang={language}`: Gets the government policies.
* `GET /api/equipment/local?lang={language}`: Gets the local technicians.
* `POST /api/equipment/help`: Gets the help/troubleshooting for equipment.
* `POST /api/medicine/advice`: Gets the medicine advice.
* `GET /api/marketing/rates?crop={crop}&location={location}&lang={language}`: Gets the market rates.
* `GET /api/marketing/storage?lang={language}`: Gets the storage locations.

## Technologies Used

* React.js
* Node.js
* Express.js
* MongoDB
* HTML5
* CSS3
* JavaScript
* Google Generative AI API
* OpenWeatherMap API
* i18next (for internationalization)
