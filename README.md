# API Gateway

This project is an API Gateway for the QuickCart application, built using Spring Boot and Spring Cloud Gateway.

## Prerequisites

- Java 11 or higher
- Maven
- Eureka Server running on `http://localhost:8761/eureka/`

## Getting Started

### Running the Application

1. Clone the repository:
    ```sh
    git clone https://github.com/MayankShivhare999/quickcart-apigateway.git
    cd quickcart-apigateway
    ```

2. Build the project using Maven:
    ```sh
    mvn clean install
    ```

3. Run the application:
    ```sh
    mvn spring-boot:run
    ```

The API Gateway will start on port `8085`.

### Configuration

The application is configured to register with Eureka Server and route requests to various services. The configuration can be found in `src/main/resources/application.properties`.

#### Eureka Configuration

- `eureka.client.service-url.defaultZone`: URL of the Eureka Server
- `eureka.instance.instance-id`: Instance ID of the API Gateway
- `eureka.instance.ip-address`: IP address of the API Gateway
- `eureka.instance.hostname`: Hostname of the API Gateway
- `eureka.instance.prefer-ip-address`: Prefer IP address over hostname
- `eureka.client.register-with-eureka`: Register with Eureka
- `eureka.client.fetch-registry`: Fetch registry from Eureka

#### Gateway Routes

- `product-service`: Routes requests with path `/products/**` to the Product Service
- `auth-service`: Routes requests with path `/auth/**` to the Auth Service
- `order-service`: Routes requests with path `/orders/**` to the Order Service
- `payment-service`: Routes requests with path `/payments/**` to the Payment Service

### License

This project is licensed under the MIT License.