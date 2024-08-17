## Description
This project is a simple payment integration system using PayPal, built with Java and Spring Boot. It allows users to make payments through PayPal using the PayPal API. The payments can be executed in either a sandbox (test) environment or a live (production) environment.

## Prerequisites
Before you begin, ensure you have the following installed:
- **Java
- **Maven
- A PayPal Developer account to create Sandbox API credentials
- An IDE such as IntelliJ IDEA or Eclipse

## Installation
Follow these steps to install and run the project locally:
1. **Clone the repository:**
     ```bash
   git clone https://github.com/your-username/paypal-integration-project.git
   cd paypal-integration-project
     ```
2. **Build the project using Maven:**
   ```
   mvn clean install
   ```
3. **Run the application:**
   ```
   mvn spring-boot:run
   ```
##Configuration
To configure the project for PayPal integration, you need to set up your PayPal credentials. This can be done in the application.yml file:
```
paypal:
  client-id: your-client-id
  client-secret: your-client-secret
  mode: sandbox

server:
  port: 8082
```
- **client-id**: Your PayPal API client ID.
- **client-secret**: Your PayPal API client secret.
- **mode**: Set this to `sandbox` for testing or `live` for production.

## Usage

1. **Access the application:** Open your browser and go to `http://localhost:8082`.

2. **Initiate a payment:** Click the "Pay with PayPal" button to start the payment process. You will be redirected to the PayPal login page to complete the transaction.

3. **Handle payment results:**
   - **Success URL**: Redirects to a success page if the payment is completed.
   - **Cancel URL**: Redirects to a cancel page if the payment is canceled by the user.
   - **Error Handling**: If an error occurs during the payment process, the user is redirected to an error page.

