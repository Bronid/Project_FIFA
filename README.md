# Analysis of the Football Likes Application
![Tekst alternatywny](https://github.com/Olaz0/pai/blob/main/photo/photo_2024-01-23_19-27-20.jpg?raw=true)
## Introduction
The application has been created to collect "likes" for football matches, where each user has a specific number of votes to use. Below is an analysis of various parts of the application.

## Setup

To run the application, use Docker and execute the following command in the terminal:

`docker-compose up --build`.

## Docker Compose
The docker-compose.yml file defines the Docker Compose configuration to run three main services: match backend, user backend, and frontend. Additionally, it uses the MongoDB database. Below is an analysis of each service:

### 1. Match Backend (`backend-match`):
- Built from the context `./match_api`.
- Runs on port 8080.
- Depends on the MongoDB service.

### 2. User Backend (`backend-user`):
- Built from the context `./user_api`.
- Runs on port 8081.
- Depends on the MongoDB service.
  
### 3. Frontend (`frontend`):
- Built from the context `./view`.
- Runs on port 80.

### 4. MongoDB (`mongo`):
- Uses the official MongoDB image.
- Runs on port 27017.

## Match Backend (`backend-match`)
- Built with Express.js.
- Uses MongoDB to store match-related data.
- Provides CRUD (Create, Read, Update, Delete) endpoints for matches.
- Includes endpoints for users to vote on specific matches.

## User Backend (`backend-user`)
- Built with Express.js.
- Uses MongoDB to store user data.
- Provides endpoints for user registration, login, and obtaining user information.

## Frontend (`frontend`)
- User interface built with HTML, CSS, and JavaScript.
- Pages include registration, login, voting on matches, displaying the list of matches, and editing them.
  
## Security
- The application uses the HTTP protocol, which may pose a security risk for transmitted data.
- Transmitting login and password in cookies (document.cookie) is not the best security practice due to the vulnerability to CSRF (Cross-Site Request Forgery) and XSS (Cross-Site Scripting) attacks.

## Conclusion
The analysis above outlines the structure and functionalities of each part of the application. It is important to note that the application aims to demonstrate the collaboration between two APIs, which is the main focus of the project. In a real production environment, additional security measures should be considered, in addition to functionality.

**Note:**
The authors of the code are aware that transmitting login and password in cookies is not a recommended security practice. In real applications, more advanced authentication and authorization methods, such as JSON Web Tokens, should be used to minimize the risk of attacks.
