# 🧾 Sistema de Gestión de Facturas

Aplicación web para la administración de facturas con autenticación de usuarios, API REST desarrollada en C# (.NET) y frontend renderizado con Flask + Jinja.

Permite gestionar clientes, facturas, usuarios y reportes de forma segura, organizada y centralizada.

---

## 🚀 Características

- Login y registro de usuarios
- Autenticación con JWT
- Gestión de roles
- CRUD de clientes
- CRUD de facturas
- Detalle de productos por factura
- API REST en C#
- Frontend con Jinja templates
- Base de datos relacional
- Arquitectura desacoplada (Frontend + API + DB)

---

## 🧱 Arquitectura

Browser (Usuario)
      ↓
Flask + Jinja (Frontend)
      ↓
ASP.NET Web API (C# Backend)
      ↓
Base de Datos

---

## 🛠️ Tecnologías

### Backend
- C# .NET (ASP.NET Web API)
- Entity Framework Core
- JWT Authentication
- Swagger

### Frontend
- Python
- Flask
- Jinja2
- HTML / CSS / JavaScript

### Base de datos
- PostgreSQL / SQL Server / MySQL

---

## 📂 Estructura del proyecto

facturacion/
│
├── backend/        # API REST .NET
├── frontend/       # Flask + Jinja
├── database/       # Scripts SQL
├── docs/
└── README.md

---

# ⚙️ Instalación

## 1. Clonar repositorio

git clone https://github.com/tu-usuario/facturacion.git
cd facturacion

---

# 🗄️ Configurar Base de Datos

Crear base de datos:

CREATE DATABASE facturacion;

Ejecutar scripts:

psql -U postgres -f database/schema.sql

(o usa tu gestor preferido)

---

# 🔹 Backend (.NET API)

## Configurar conexión

Editar:

backend/appsettings.json

{
  "ConnectionStrings": {
    "DefaultConnection": "Host=localhost;Database=facturacion;Username=postgres;Password=1234"
  },
  "Jwt": {
    "Key": "super_secret_key"
  }
}

## Instalar dependencias

cd backend
dotnet restore

## Ejecutar servidor

dotnet run

API disponible en:
http://localhost:5000

Swagger:
http://localhost:5000/swagger

---

# 🔹 Frontend (Flask + Jinja)

## Instalar dependencias

cd frontend
pip install -r requirements.txt

## Ejecutar aplicación

python app.py

Disponible en:
http://localhost:3000

---

# 🔐 Autenticación

Se utiliza JWT.

Flujo:
1. Usuario inicia sesión
2. API devuelve token
3. Frontend guarda token en sesión/cookies
4. Token se envía en cada request

Header requerido:

Authorization: Bearer <token>

---

# 📡 Endpoints principales

## Auth
POST   /api/auth/login
POST   /api/auth/register
GET    /api/auth/profile

## Clientes
GET    /api/clients
POST   /api/clients
PUT    /api/clients/{id}
DELETE /api/clients/{id}

## Facturas
GET    /api/invoices
POST   /api/invoices
GET    /api/invoices/{id}
PUT    /api/invoices/{id}
DELETE /api/invoices/{id}

---

# 🗄️ Modelo de Base de Datos

## users
- id
- name
- email
- password_hash
- role

## clients
- id
- name
- document
- phone

## invoices
- id
- client_id
- user_id
- date
- total

## invoice_items
- id
- invoice_id
- description
- price
- quantity

---

# 🧪 Pruebas

Backend:
dotnet test

Frontend:
pytest

---

# 🚀 Despliegue

Opciones:
- Backend → Azure / Render / Railway
- Frontend → VPS / Render
- DB → Supabase / Neon / Azure SQL

O con Docker:

docker-compose up --build

---

# 🤝 Contribuir

1. Fork
2. Crear rama
3. Commit
4. Pull Request

---

# 📄 Licencia

MIT
