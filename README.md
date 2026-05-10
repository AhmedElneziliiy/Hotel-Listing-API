# Hotel Listing API

A **RESTful ASP.NET Core Web API** for managing hotels and countries — with JWT authentication, API versioning, global error handling, and paginated responses.

## What it does

Exposes endpoints to list, create, update, and delete hotels and the countries they belong to. Users must register and authenticate with a JWT token to access protected endpoints. The API supports versioning and returns paginated results for large datasets.

## Tech Stack

- **ASP.NET Core Web API** (.NET)
- **Entity Framework Core** — Code-First with SQL Server
- **ASP.NET Identity** — user registration and JWT token issuance
- **AutoMapper** — entity ↔ DTO mapping
- **API Versioning** — v1 and v2 country endpoints
- **Serilog** — structured logging
- **Swagger / OpenAPI**

## Key Features

- Country and Hotel CRUD endpoints
- JWT-based authentication (`/api/account/login`, `/api/account/register`)
- API versioning (v1 / v2 for countries)
- Global exception middleware
- Paginated results with `RequestParams` (PageNumber, PageSize)
- EF Core seeding for countries and hotels

## Getting Started

1. Set your SQL Server connection string and JWT config in `appsettings.json`.
2. Apply migrations:
   ```bash
   dotnet ef database update
   ```
3. Run the API:
   ```bash
   dotnet run --project HotelListing
   ```
4. Open Swagger at `https://localhost:{port}/swagger`.
