# Airbnb Clone Project

## Project Overview
The **Airbnb Clone Project** is a comprehensive, real-world web application designed to replicate the core functionalities, scalability, and user experience of the Airbnb platform. It emphasizes full-stack development practices including backend systems, database architecture, API security, and DevOps integration.

## Project Goals
This project aims to:

- Simulate real-world software development with a scalable, modular architecture.  
- Deepen understanding of backend systems and relational database design.  
- Apply secure API development practices to protect user data and ensure safe transactions.  
- Implement responsive UI/UX designs for a seamless user experience across devices.  

## Technology Stack 

> The project integrates a modern, scalable, and secure technology stack designed for full-stack development and microservice-oriented architecture.

### Backend
- **Django** – Robust backend framework for scalable and secure web APIs.  
- **GraphQL** – Query language for APIs providing flexible and efficient data fetching.  
- **Redis** – In-memory data store for caching and task queueing.  
- **Celery** – Asynchronous task queue/job queue based on distributed message passing.  
- **Kafka / RabbitMQ** – Message brokers for reliable event-driven communication.  
- **Docker** – Containerization for consistent development and deployment environments.  
- **Kubernetes** – Orchestration of containerized applications at scale.  
- **PostgreSQL** – Relational database with strong consistency and performance.  
- **Prometheus + Grafana** – Monitoring and visualization stack for system performance.

### Frontend
- **React** – Component-based UI library for building dynamic user interfaces.  
- **Tailwind CSS** – Utility-first CSS framework for fast and responsive styling.  
- **TypeScript** – Strongly typed JavaScript to enhance code quality and maintainability.  
- **Shadcn** – UI component library for elegant and accessible design.



## Project/team Roles and Responsibilities

| **Role**              | **Responsibilities**                                                                 |
|-----------------------|--------------------------------------------------------------------------------------|
| Project Manager       | Oversees timeline, coordinates team, manages deliverables                           |
| Frontend Developers   | Implements UI components, ensures responsive design                                 |
| Backend Developers    | Builds APIs, manages database, implements business logic                            |
| Designers             | Creates mockups, maintains design system, ensures UX quality                        |
| QA/Testers            | Writes test cases, performs testing, reports bugs                                   |
| DevOps Engineers      | Manages deployment, CI/CD pipeline, server infrastructure                           |
| Product Owner         | Defines requirements, prioritizes features, represents stakeholders                 |
| Scrum Master          | Facilitates agile processes, removes blockers, organizes meetings                   |



## Backend Structure

### Database Design

#### Tables & Fields

- **Users:** `id`, `full_name`, `address`, `phone_number`
- **Properties:** `id`, `user_id`, `description`, `number_of_bedrooms`, `price_per_night`, `address`
- **Bookings:** `id`, `property_id`, `user_id`, `check_in_date`, `check_out_date`, `price`, `discount`  
- **Reviews:** `id`, `user_id`, `property_id`, `rating`, `comment`, `created_at`  
- **Payments:** `id`, `booking_id`, `amount`, `payment_date`

#### Database Relationships

- A **user** can own multiple **properties**.
- A **booking** belongs to one **property** and one **user**.
- A **user** can leave one **review** per **property**.
- A **property** can have many **reviews**.
- A **payment** is associated with one **booking**, and a **user** can make multiple payments.

