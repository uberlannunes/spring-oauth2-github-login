# Login with GitHub Profile 

This project demonstrates how to implement GitHub OAuth2 login in a web application. It allows users to authenticate using their GitHub credentials.

## Technology Stack

The project utilizes the following technologies and frameworks:

- Java
- Spring Boot
- Spring Security
- OAuth2
- Maven (for build and dependency management)

## Prerequisites

Before running this project, make sure you have the following prerequisites:

- Java JDK (version 17 or higher)
- Maven (for building and managing dependencies)
- GitHub account (to create an OAuth App)

## Setup

1. Clone the repository:
```bash
git clone https://github.com/uberlannunes/spring-oauth2-github-login.git
```

2. Navigate to the project directory:
```bash
cd spring-oauth2-github-login
```

3. Create a GitHub OAuth App:

> 1. Go to your GitHub account settings
Navigate to "Developer settings" > "OAuth Apps"
> 2. Click on "Register a new application".
> 3. Enter the required details (App name, Homepage URL (http://localhost:8080), Authorization callback URL(http://localhost:8080/login/oauth2/code/github))
> 4. Save the changes and note down the generated Client ID and Client Secret


4. Configure the application properties:
> 1. Open src/main/resources/application.properties
> 2. Set the "spring.security.oauth2.client.registration.github.clientId" property to your GitHub OAuth App's Client ID
> 3. Set the "spring.security.oauth2.client.registration.github.clientSecret" property to your GitHub OAuth App's Client Secret


5. Run the Application
```bash
./mvnw spring-boot:run
```

## Usage
1. Open a web browser and navigate to http://localhost:8080
2. Click on the "Login with GitHub" button to initiate the OAuth2 login process.
3. After successful authentication, the application will display the user's GitHub profile information.
