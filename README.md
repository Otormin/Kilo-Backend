```md
# ⚡ Kilo Backend API

[![.NET 8](https://img.shields.io/badge/.NET-8.0-512bd4?logo=dotnet)](https://dotnet.microsoft.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Deployed to Azure](https://img.shields.io/badge/Deployed%20to-Azure-0089D6?logo=microsoftazure)](https://azure.microsoft.com/)

**Kilo** is a high-performance backend API built with **ASP.NET Core** that facilitates a decentralized energy marketplace. It enables users to buy and sell surplus solar/wind energy (kWh) through automated listing management and real-time transaction tracking.

---

## 🚀 Features

- **Energy Marketplace:** Create, manage, and discover energy listings based on location.
- **Transaction Engine:** Secure lifecycle management for buying/selling energy.
- **Real-Time Tracking:** Dynamic kWh tracking and automated delivery processing.
- **Meter Integration:** Tracks total generation vs. consumption to calculate available surplus.
- **Background Workers:** Hosted services manage energy delivery asynchronously.
- **Enterprise Logging:** Robust error tracking and system health monitoring via **NLog**.

---

## 🏗️ Tech Stack

- **Framework:** ASP.NET Core (.NET 8)
- **Database:** Azure SQL / SQL Server
- **ORM:** Entity Framework Core (Code First)
- **Deployment:** Azure App Service (Linux)
- **CI/CD:** GitHub Actions (Automated Deployment on Push)
- **API Documentation:** Swagger / OpenAPI
- **Security:** IP-based Rate Limiting, Forwarded Headers, and RowVersion Concurrency Control

---

## 📂 Project Architecture

The project follows a clean, layered architecture:

```

Kilo/
├── Data/           # DbContext and Migrations
├── Controllers/    # API Endpoints
├── Services/       # Business Logic Layer
├── Repository/     # Data Access Layer
├── Models/         # Database Entities
├── DTOs/           # Data Transfer Objects
├── Mappers/        # Mapping Logic
└── Helpers/        # Utilities & Background Services

```

---

## 🔐 Security & Optimization

- **Rate Limiting:** Sliding window policy per User IP to prevent API abuse  
- **Azure Ready:** Uses `ForwardedHeaders` for correct client IP detection  
- **Environment Safety:** `.env` for local dev, Azure env vars for production  
- **Concurrency:** `RowVersion` to prevent double transactions  

---

## 🧪 API Documentation

The API is fully documented with Swagger. Once running, visit:

```

/swagger

```

---

## 📸 Swagger Screenshots

<img src="Screenshots/kilo1.png"/>
<img src="Screenshots/kilo2.png"/>
<img src="Screenshots/kilo3.png"/>
<img src="Screenshots/kilo4.png"/>

---

## 🔄 CI/CD Pipeline

This project uses **GitHub Actions**:

1. Build application  
2. Publish artifacts  
3. Deploy to Azure App Service  

---

## 👨‍💻 Author

Developed by **Young Jesse (GitHub: Otormin)**  
Backend engineer for the Kilo energy trading platform.
```