# LearningMap — .NET API

LearningMap is a backend API developed in **.NET** that helps users structure their own **learning projects** based on **metalearning** map principles.

Each **map/project** contains organized information about **Knowledge**, **Strategy**, and **Motivation**, making the learning process planned and much more efficient.

---

## Technologies Used

* **.NET 8**
* **ASP.NET Core Web API**
* **Entity Framework Core**
* **ASP.NET Core Identity**
* **JWT Bearer Authentication**
* **AutoMapper**
* **Pagination**
* **SQL Server**
* **xUnit and FluentAssertions (Testing)**

---

## Features

### Authentication & Authorization

* User registration with credential validation.
* Login with **JWT** token generation.
* Role-based access control (`user`).

### Learning Maps/Projects

* Create new maps/projects containing **Knowledge**, **Strategy**, and **Motivation**.
* Query all maps or a specific one by ID.
* Update or remove maps.
* Map pagination with header metadata (`X-Pagination`).

### Knowledge

* Register items the user wants to learn within a map/project.
* Query knowledge items by ID or by map/project.
* Update and remove knowledge items.
* Result pagination with header metadata (`X-Pagination`).

### Strategy

* Register learning strategies for each map/project.
* Query strategies by ID or by map/project.
* Update and remove strategies.
* Result pagination with header metadata (`X-Pagination`).

### Motivation

* Register motivations that guide the learning process.
* Query motivations by ID or by map/project.
* Update and remove motivations.
* Result pagination with header metadata (`X-Pagination`).

---

## Main Endpoints

### Auth

* `POST /api/auth/register` → Register a new user.
* `POST /api/auth/login` → Authenticate user and generate a JWT token.

### Maps/Projects

* `GET /api/projeto` → List all maps/projects.
* `GET /api/projeto/{id}` → Get a map/project by ID.
* `GET /api/projeto/pagination` → List maps/projects with pagination.
* `POST /api/projeto` → Create a basic new map/project.
* `POST /api/projeto/completo` → Create a complete map/project with **Knowledge**, **Strategy**, and **Motivation**.
* `PUT /api/projeto/{id}` → Update a map/project.
* `DELETE /api/projeto/{id}` → Delete a map/project.

### Knowledge

* `GET /api/conhecimento` → List all knowledge items.
* `GET /api/conhecimento/{id}/conhecimento` → Get a knowledge item by ID.
* `GET /api/conhecimento/{id}/projeto` → Get knowledge items for a map/project.
* `GET /api/conhecimento/pagination` → List knowledge items with pagination.
* `POST /api/conhecimento` → Create a knowledge item.
* `PUT /api/conhecimento/{projetoId}/conhecimento/{id}` → Update a knowledge item.
* `DELETE /api/conhecimento/{projetoId}/conhecimento/{id}` → Remove a knowledge item.

### Strategy

* `GET /api/estrategia` → List all strategies.
* `GET /api/estrategia/{id}/estrategia` → Get a strategy by ID.
* `GET /api/estrategia/{id}/projeto` → Get strategies for a map/project.
* `GET /api/estrategia/pagination` → List strategies with pagination.
* `POST /api/estrategia` → Create a strategy.
* `PUT /api/estrategia/{projetoId}/estrategia/{id}` → Update a strategy.
* `DELETE /api/estrategia/{projetoId}/estrategia/{id}` → Remove a strategy.

### Motivation

* `GET /api/motivacao` → List all motivations.
* `GET /api/motivacao/{id}/motivacao` → Get a motivation by ID.
* `GET /api/motivacao/{id}/projeto` → Get motivations for a map/project.
* `GET /api/motivacao/pagination` → List motivations with pagination.
* `POST /api/motivacao` → Create a motivation.
* `PUT /api/motivacao/{projetoId}/motivacao/{id}` → Update a motivation.
* `DELETE /api/motivacao/{projetoId}/motivacao/{id}` → Remove a motivation.
