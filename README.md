# chatbot

This project is a Java-based chatbot application that integrates with Swagger for API documentation. The chatbot interacts with external services like Amazon and a weather API to provide responses based on user queries. The application is built using Spring Boot and incorporates Swagger for clear API documentation.

Project Overview
Swagger UI Endpoint: Swagger UI
Heroku Deployment: Heroku App (Fork the project and deploy it to your Heroku account)
Table of Contents
Dependencies
Project Structure
Swagger Integration
Usage
External APIs
Deployment
Important Note
Dependencies
The project uses Maven for dependency management. Notable dependencies include:

Springfox Swagger: Version 2.6.1 - Used for API documentation.
OkHttp: Version 4.8.1 - HTTP client for making requests.
Squareup OkHttp3: Version 4.8.1 - HTTP client used in AmazonService.
Project Structure
config/SwaggerConfig.java: Configuration class for Swagger integration.
controller/BotController.java: Controller class defining REST endpoints for the chatbot.
service/AmazonService.java: Service class for interacting with Amazon product search.
service/WeatherService.java: Service class for obtaining weather information.
Swagger Integration
Swagger is integrated into the project to provide clear and interactive API documentation. Access the Swagger UI at http://localhost:8080/swagger-ui.html# after starting the application.

Usage
Amazon Product Search:

Endpoint: /bot/amazon
Method: GET
Parameter: keyword - The product keyword to search on Amazon.
Weather Information:

Endpoint: /bot
Method: POST
Request Body: BotQuery - The query structure containing user input.
Supported Queries:
{"city": "CityName"} - Retrieves weather information for the specified city.
{"product": "ProductName"} - Searches for products on Amazon based on the provided product name.
External APIs
Amazon Product Search:

The application uses OkHttp to make a request to the Amazon search page and retrieve HTML content.
Regex is used to extract product information from the HTML response.
Weather Information:

The application interacts with Yahoo Weather API to obtain weather details for a specified location.
The API response is parsed to extract relevant weather information.
Deployment
The project is ready for deployment and includes a reference to Heroku. Fork the project and deploy it to your preferred hosting platform.

Important Note
The weather API used in the project may change over time, so ensure that the weather service implementation is up-to-date with the API changes.
