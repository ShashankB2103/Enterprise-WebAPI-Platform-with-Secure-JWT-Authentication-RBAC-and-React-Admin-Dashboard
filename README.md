# **Enterprise RBAC Platform – ASP.NET Core WebAPI & React Admin Dashboard**

This project is an enterprise-grade **Role-Based Access Control (RBAC) platform** built using **ASP.NET Core WebAPI**, **React**, and **Redux**.  
It provides a secure authentication and authorization system with dynamic role and permission management, fully configurable through an admin dashboard.

The system follows a **microservice-ready architecture**, supports **SQL Server**, **MongoDB**, and **Redis**, and includes Docker configuration for easy deployment.

---

## 🚀 **Features**

### 🔐 Authentication & Authorization
- Secure **JWT authentication**
- Multi-role support
- Dynamic **RBAC (Role-Based Access Control)**
- Permission-based UI & API access

### 🧑‍💼 Admin Panel
- Manage users, roles, and permissions
- No hardcoded permissions — fully configurable
- Frontend + backend enforcement

### 🏗 Architecture
- ASP.NET Core WebAPI (Auth & Resource servers)
- React/Redux frontend
- Microservice-friendly structure
- Modular and scalable design

### 🗄 Databases & Caching
- **SQL Server** (Primary data store)
- **MongoDB** (Document store)
- **Redis** (Caching)

### 🐳 Docker Support
- Containers for SQL Server, MongoDB, and Redis
- Easy local development and testing

---

## 📁 **Project Structure**

```
/client                       → React Admin Dashboard
/server/AuthWebApplication    → Authentication microservice
/server/WebApplication2       → Resource/API microservice
/artifacts/docker             → Docker compose & environment files
```

---

## ⚙️ **Prerequisites**

Ensure the following are installed:

- Node.js (v16+)
- .NET 6 SDK or later
- Docker Desktop
- SQL Server (optional if using Docker)
- MongoDB (optional if using Docker)

---

## 🐳 **Running with Docker (Recommended)**

Navigate to the docker folder:

```sh
cd artifacts/docker
docker-compose up -d
```

This will automatically start:
- SQL Server  
- MongoDB  
- Redis  

---

## ▶️ **Run the Auth Server**

```sh
cd server/AuthWebApplication/AuthWebApplication
dotnet restore
dotnet run
```

Default URL:
```
https://localhost:5001/
```

---

## ▶️ **Run the Resource Server**

```sh
cd server/WebApplication2/WebApplication2
dotnet restore
dotnet run
```

Default URL:
```
https://localhost:5003/
```

---

## ▶️ **Run the Client (React Dashboard)**

```sh
cd client
npm install
npm start
```

Default URL:
```
http://localhost:3000/
```

---

## 🛡 **Security Overview**

- JWT token validation for all protected APIs  
- Middleware-based permission enforcement  
- Frontend route protection using Redux  
- Fine-grained role & permission mapping  

---

## 📌 **Future Enhancements**
- Add audit logging  
- Email/SMS notification service  
- Add PostgreSQL support  
- Add unit and integration tests  

---

