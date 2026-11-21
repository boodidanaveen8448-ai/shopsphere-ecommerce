# ShopSphere

Full-stack e-commerce starter with product catalog and order management.

## Features
- Product catalog CRUD
- Stock quantity tracking
- REST API with validation
- React product dashboard
- PostgreSQL-ready Docker setup

## Tech stack
- Java 17, Spring Boot 3.4, Spring Data JPA, Bean Validation
- React, TypeScript, Vite
- H2 for quick local development; PostgreSQL driver included for deployment
- RESTful CRUD API

## Run locally

### Backend
Requirements: JDK 17+ and Maven.

```bash
cd backend
mvn spring-boot:run
```
API: `http://localhost:8080/api/products`

H2 console: `http://localhost:8080/h2-console` (JDBC URL: `jdbc:h2:mem:portfolio_db`, username `sa`, blank password).

### Frontend
In a second terminal:

```bash
cd frontend
npm install
npm run dev
```
Open `http://localhost:5173`.

## API endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/products` | List all |
| GET | `/api/products/{id}` | Get one |
| POST | `/api/products` | Create |
| PUT | `/api/products/{id}` | Update |
| DELETE | `/api/products/{id}` | Delete |

## Example request

```json
{
  "name": "Wireless Headphones",
  "description": "Bluetooth over-ear headphones",
  "price": 79.99,
  "stock": 25
}
```

## Suggested next improvements
- Add Spring Security with JWT and role-based access control.
- Add service-layer business rules and centralized exception responses.
- Add unit/integration tests and API documentation with OpenAPI.
- Add Docker Compose for the app and PostgreSQL.
- Add CI with GitHub Actions and deploy a demo.

## Important
This repository is a working CRUD MVP foundation, not a production payment, hiring, or ordering system. Do not claim payment processing, authentication, or other features until you implement and test them.
