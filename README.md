# Hotel Booking System

## Introduction

This project is a hotel booking system built using **NestJS** and follows a **microservice architecture**. It is designed to handle various functionalities such as authentication, reservations, payments, and notifications. The system is built with scalability, maintainability, and modularity in mind, leveraging modern frameworks and best practices.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Architecture](#architecture)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/wiwiewei18/be-hotel-reservation.git
   cd be-hotel-reservation
   ```

2. **Set up environment variables:**
   Create a `.env` file in the root directory of each service and add the necessary environment variables. A sample `.env.example` file is provided in each service directory for reference.

3. **Build and run the services:**

   ```bash
   docker-compose build
   docker-compose up
   ```

## Usage

1. **Start the development server:**

   ```bash
   docker-compose watch
   ```

2. **Run the end-to-end tests:**

   ```bash
   cd e2e
   docker-compose up
   ```

3. **Start the production server:**

   ```bash
   docker-compose up
   ```

## Features

- **Microservice Architecture:** Independent services for authentication, reservations, payments, and notifications.
- **Scalable Design:** Modular and decoupled services for easier scaling and maintenance.
- **Comprehensive Functionality:** Includes features like user authentication, hotel reservations, payment processing, and email notifications.
- **Environment Configurations:** Simplified management of service-specific environment variables.

## Architecture

The system is divided into multiple microservices:

- **Auth Service:** Handles user authentication and authorization using `@nestjs/passport` and `bcrypt`.
- **Reservations Service:** Manages hotel reservations and availability.
- **Payments Service:** Processes payments using `Stripe`.
- **Notifications Service:** Sends email notifications using `Nodemailer`.

Each service operates independently and communicates via **NestJS Microservices**.

## Dependencies

- **@nestjs/microservices**: Facilitates building microservice applications.
- **mongoose**: For MongoDB interactions.
- **express**: Web framework for handling routes and middleware.
- **jest**: Testing framework.
- **supertest**: HTTP assertions for API testing.
- **bcrypt**: Password hashing.
- **passport**: Authentication middleware.
- **nodemailer**: Email sending.
- **stripe**: Payment processing.

## Configuration

Configuration files include:

- `.env`: Environment variables for each service.

## Documentation

- **[API Documentation](https://documenter.getpostman.com/view/17226825/2sAYJ7eyUk):** Detailed documentation for the API endpoints.

## Troubleshooting

- **Services not starting:**

  - Ensure Docker is installed and running.
  - Verify that all `.env` files are correctly configured.
  - Review logs for specific error messages.

- **Environment variables not loading:**
  - Confirm `.env` files exist in each service directory and variables are correctly defined.
  - Restart the services to reload environment variables.

## Contributors

- **Wiwie Sanjaya** - Initial work - [wiwiewei18@gmail.com](mailto:wiwiewei18@gmail.com)
