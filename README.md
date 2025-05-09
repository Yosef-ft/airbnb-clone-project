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



## Project Roles and Responsibilities
## Team Roles

| **Role**              | **Responsibilities**                                                                 |
|-----------------------|--------------------------------------------------------------------------------------|
| Project Manager       | Oversees timeline, coordinates team, manages deliverables                           |
| Frontend Developers   | Implements UI components, ensures responsive design                                 |
| Backend Developer     | Builds APIs, manages database, implements business logic                            |
| Database Administrator| Ensure data integrity, availability, and performance                                |
| UI/UX designer        | Transforms a product vision into user-friendly designs                              |
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




### Feature Breakdown
1. **User Management**  
   - Manage guest ratings  
   - Manage host profiles  

2. **Property Management**  
   - Manage available properties  
   - Define and enforce property rules  

3. **Booking System**  
   - Handle booking creation and cancellation  
   - Manage guest check-ins and check-outs  

4. **User Feedback**  
   - Manage complaints  
   - Handle property reviews and ratings  


### API Security
- **Authentication** – Verifying the identity of users before granting access  
- **Authorization** – Controlling access to resources based on user roles and permissions  
- **Rate Limiting** – Throttling requests to prevent abuse, DDoS, or brute force attacks  

#### Why security is crucial
- Protects sensitive **user data** from unauthorized access  
- Secures **payment information** and transaction integrity  
- Maintains **system integrity** by preventing malicious API misuse 


### CI/CD Pipeline
- A well-configured CI/CD pipeline enables **continuous integration and continuous delivery**, allowing teams to automatically build, test, and deploy new features with confidence and speed. This streamlines the development workflow, reduces manual errors, and ensures faster delivery of updates to production.

#### Tools Commonly Used

- **GitHub Actions** – Automates workflows for building, testing, and deploying code  
- **Docker** – Ensures consistent containerized environments across all stages  
- **Kubernetes** – Manages container orchestration for scalable deployments  



## Frontend Structure

### UI/UX Design Planning
#### Design Goals
- Create intuitive booking flow
- Maintain visual consistency
- Ensure fast loading times
- Prioritize mobile responsiveness

#### Key Features
- Property search and filtering
- Detailed property viewing
- Secure checkout process
- User authentication

#### Primary Pages
| Page                   | Description                                                         |
|------------------------|---------------------------------------------------------------------|
| Property Listing View  | Displays available properties in a grid format with filtering options |
| Listing Detail View    | Shows complete details of a selected property including images and booking form |
| Simple Checkout View   | Provides a clean interface for making payments and confirming bookings |


#### Importance of User-Friendly Design
An intuitive and responsive user interface enhances the booking experience, helping users navigate seamlessly from discovery to checkout. 


### Figma Design Specifications

#### Color Styles

| Style           | Hex Code   |
|----------------|------------|
| **Primary**     | `#FF5A5F`  |
| **Secondary**   | `#008489`  |
| **Background**  | `#FFFFFF`  |
| **Text**        | `#222222`  |
| **Secondary Text** | `#717171` |

---

#### Typography

| Element           | Font        | Weight      | Size      |
|------------------|-------------|-------------|-----------|
| **Primary Font**  | Circular    | Medium (500)| 16px      |
| **Headings**      | Circular    | Bold (700)  | 24px–32px |
| **Secondary Text**| Circular    | Book (400)  | 14px      |


### UI Component Patterns

#### 1. Navbar
- Logo
- Search bar
- User navigation
- Responsive menu

#### 2. Property Card
- Property image
- Basic details (price, location, rating)
- Favorite button
- Responsive layout

#### 3. Footer
- Site links
- Company information
- Social media links
- Copyright information
