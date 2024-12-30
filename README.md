# Hotel Reservation Microservices Backend

## Overview

This project implements a backend platform for a hotel reservation platform using a microservices architecture built with [NestJS](https://nestjs.com/). Each microservice communicates via TCP using the `@nestjs/microservices` package. The project is containerized with Docker and orchestrated using Kubernetes.

## Features

- **Microservices Architecture**: Independent services for handling reservations, user management, payment processing, and notifications.
- **TCP Communication**: Secure and efficient communication between microservices.
- **Containerization**: Each microservice runs in its own Docker container.
- **Orchestration**: Kubernetes manages scaling, deployment, and service discovery.

## Tech Stack

- **Framework**: [NestJS](https://nestjs.com/)
- **Communication**: `@nestjs/microservices` (TCP)
- **Containerization**: Docker
- **Orchestration**: Kubernetes
- **Database**: MongoDB

## Services

1. **User Service**: Manages user registration, authentication, and profiles.
2. **Reservation Service**: Handles booking, editing bookings, and deleting bookings.
3. **Payment Service**: Processes payments and manages payment statuses.
4. **Notification Service**: Sends email notifications for booking confirmations and updates.

## Project Structure

```
project-root/
├── apps/
│   ├── auth/
│   ├── notifications/
│   ├── payments/
│   └── reservations/
├── k8s/
├── libs/
│   └── common/ (shared libraries and utilities)
├── package.json
└── README.md
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- [Docker](https://www.docker.com/)
- [Kubernetes](https://kubernetes.io/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

### Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/wiwiewei18/be-hotel-reservation.git
   cd be-hotel-reservation
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Set environment variables**:
   Copy `.env.example` to `.env` and fill in the necessary values.

4. **Run the services locally**:
   ```bash
   docker-compose up --build
   ```
