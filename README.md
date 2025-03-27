# Email Writer Project

## Overview
This project consists of an Email Writer system, which includes:
1. **email-writer-ext**: A browser extension that integrates with Gmail to generate AI-powered email replies.
2. **email-writer-sb**: A Spring Boot backend that processes email content and generates responses using AI.

## Features
- The browser extension injects an **AI Reply** button in the Gmail compose window.
- Fetches email content and sends it to the backend API for AI-generated responses.
- Spring Boot backend processes the request and returns an AI-generated email response.

## Installation & Setup
### 1. Clone the Repository
```sh
git clone https://github.com/your-username/email-writer.git
cd email-writer
```

### 2. Setting up the Spring Boot Backend
#### Prerequisites:
- Java 17+
- Maven

#### Steps:
```sh
cd email-writer-sb
mvn clean install
mvn spring-boot:run
```
The backend should start running at `http://localhost:8080`.

### 3. Setting up the Chrome Extension
#### Steps:
1. Open **Chrome** and go to `chrome://extensions/`
2. Enable **Developer Mode** (toggle on the top right).
3. Click **Load Unpacked** and select the `email-writer-ext` folder.
4. The extension will be loaded, and the **AI Reply** button should appear in Gmail.

## API Endpoints
- `POST /api/email/generate` - Accepts email content and returns an AI-generated reply.

## Deployment
To deploy the backend on **Heroku**, follow these steps:
```sh
heroku create email-writer-sb
heroku deploy:jar target/email-writer-sb.jar
```

## Contributing
Feel free to fork this repository and contribute! Pull requests are welcome.
