# E-commerce-Microservices-App


## What are we going to build ?

* A Free Marketplace where sellers can craete gigs and buyers can purchase gigs or custom gigis.

### Project Architecture 

<img src="/public/images/Project-Architecture.png">

### subdomains
 
<img src="/public/images/subdomains.png">

### functional requirements : describe what system should do

<img src="/public/images/functional-requirements.png">

###  Nonfunctional Requirements

<img src="/public/images/Nonfunctional-requirements.png">

### Design Decision

<img src="/public/images/Design-decision.png">

### Inter Process Communication

<img src="/public/images/inter-process-communication.png">


# Microservices with NodeJS, React, TypeScript, and Kubernetes

Welcome to the project repository for the Udemy course **Microservices with NodeJS, React, TypeScript, and Kubernetes**. This project involves building an advanced e-commerce marketplace application leveraging a microservices architecture. Below, you'll find a detailed description of the skills and technologies used in this project.

## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Technologies and Skills](#technologies-and-skills)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [API Documentation](#api-documentation)
- [Deployment](#deployment)
- [Testing](#testing)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project demonstrates the development of a sophisticated e-commerce marketplace application using modern technologies and tools. The architecture is based on microservices, enabling scalability and maintainability. Each microservice is developed with NodeJS and Express, containerized with Docker, and orchestrated with Kubernetes.

## Project Structure

```
/project-root
    /auth-service
    /product-service
    /order-service
    /common
    /client
    /infra
    docker-compose.yml
    README.md
```

### /auth-service

Handles user authentication and authorization.

### /product-service

Manages product listings and details.

### /order-service

Processes and manages customer orders.

### /common

Contains shared utilities and models.

### /client

The frontend application built with React.

### /infra

Infrastructure-related configurations and files.

## Technologies and Skills

### Frontend

- **React**: Building an amazing e-commerce marketplace application.
- **TypeScript**: Ensuring type safety and robustness in the frontend code.
- **Redux Toolkit RTK Query**: Efficient data fetching and caching.

### Backend

- **NodeJS and Express**: Developing and designing REST APIs.
- **TypeScript**: Ensuring type safety and robustness in the backend code.
- **MongoDB, MySQL, PostgreSQL**: Using multiple databases for different services.

### Microservices and Orchestration

- **Docker**: Creating containers for microservices.
- **Kubernetes**: Orchestrating microservices on Minikube and AWS EKS clusters.

### CI/CD

- **Jenkins**: Setting up Continuous Integration/Delivery pipelines both locally and on the cloud.

### Communication and Monitoring

- **RabbitMQ**: Setting up microservices communication.
- **Elasticsearch, Kibana, Prometheus, Grafana**: Implementing observability and monitoring.

### Additional Tools

- **Redis**: Using for caching.
- **Docker Compose**: Setting up services locally.
- **JWT**: Setting up access to microservices using JWT-based authentication.

## Getting Started

### Prerequisites

- Node.js
- Docker
- Kubernetes
- Minikube
- Skaffold
- Jenkins

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install dependencies for each service:
   ```bash
   cd auth-service
   npm install
   cd ../product-service
   npm install
   cd ../order-service
   npm install
   ```

3. Set up environment variables:
   - Create `.env` files in each service directory.
   - Example for `auth-service`:
     ```
     MONGO_URI=mongodb://<mongo-url>
     JWT_KEY=<your-jwt-key>
     ```

## Running the Application

### Running Locally

1. Start the services using Docker Compose:
   ```bash
   docker-compose up
   ```

2. Access the frontend application at `http://localhost:3000`.

### Running with Kubernetes

1. Start Minikube:
   ```bash
   minikube start
   ```

2. Deploy the services with Skaffold:
   ```bash
   skaffold dev
   ```

3. Access the frontend application at the Minikube IP.

## API Documentation

### Authentication Service

- **POST /api/users/signup**: Create a new user.
- **POST /api/users/signin**: Authenticate a user.

### Product Service

- **GET /api/products**: List all products.
- **POST /api/products**: Create a new product.

### Order Service

- **POST /api/orders**: Create a new order.
- **GET /api/orders**: List all orders.

## Deployment

### Production Deployment

1. Build Docker images for each service:
   ```bash
   docker build -t <your-dockerhub-username>/auth-service .
   docker build -t <your-dockerhub-username>/product-service .
   docker build -t <your-dockerhub-username>/order-service .
   ```

2. Push Docker images to Docker Hub:
   ```bash
   docker push <your-dockerhub-username>/auth-service
   docker push <your-dockerhub-username>/product-service
   docker push <your-dockerhub-username>/order-service
   ```

3. Deploy to Kubernetes cluster:
   ```bash
   kubectl apply -f k8s/
   ```

## Testing

### Unit Tests

1. Run unit tests for each service:
   ```bash
   cd auth-service
   npm test
   cd ../product-service
   npm test
   cd ../order-service
   npm test
   ```

### Integration Tests

Describe how to run integration tests if applicable.

## Troubleshooting

Common issues and their solutions.

### Docker Issues

Describe potential Docker issues and how to resolve them.

### Kubernetes Issues

Describe potential Kubernetes issues and how to resolve them.

## Contributing

Guidelines for contributing to the project.

### Code of Conduct

State the code of conduct for contributors.

### How to Contribute

Describe how to fork the repository, create a branch, make changes, and submit a pull request.

## License

Include the license under which the project is distributed.

---

This README.md file provides a comprehensive overview of the project, covering its structure, technologies used, setup instructions, and more. Feel free to customize it further to suit your project's needs.




