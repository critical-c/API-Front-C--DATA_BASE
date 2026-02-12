# 📊 Sistema de Gestión de Proyectos

Aplicación web para la administración y seguimiento de proyectos, actividades, presupuestos, entregables y responsables.

El sistema está compuesto por:

- Backend API REST en C# (.NET)
- Frontend web
- Base de datos relacional (bdproyecto)

Repositorio:
https://github.com/critical-c/API-Front-C--DATA_BASE.git

---

## 🚀 Funcionalidades

- Autenticación de usuarios (login)
- Gestión de proyectos
- Control de actividades
- Manejo de presupuestos
- Seguimiento de ejecución presupuestal
- Gestión de entregables
- Asignación de responsables
- Carga de archivos
- Estados de proyectos y tareas
- API REST desacoplada del frontend

---

## 🧱 Arquitectura

Usuario (Navegador)
      ↓
Frontend
      ↓
API REST (.NET C#)
      ↓
Base de Datos (bdproyecto)

Arquitectura cliente-servidor desacoplada.

---

## 🛠️ Tecnologías

### Backend
- C# .NET / ASP.NET Web API
- Entity Framework Core
- JWT Authentication
- Swagger

### Frontend
- HTML / CSS / JavaScript
- (Plantillas o framework del proyecto)

### Base de datos
- PostgreSQL / SQL Server / MySQL

---

## 📂 Estructura del proyecto

```
API-Front-C--DATA_BASE/
│
├── backend/        # API C#
├── frontend/       # Cliente web
├── database/       # Scripts SQL
└── README.md
```

---

# ⚙️ Instalación

## 1. Clonar repositorio

```
git clone https://github.com/critical-c/API-Front-C--DATA_BASE.git
cd API-Front-C--DATA_BASE
```

---

# 🗄️ Base de Datos

Nombre:

```
bdproyecto
```

Crear:

```
CREATE DATABASE bdproyecto;
```

Ejecutar scripts SQL del directorio `database/`.

---

# 🔹 Backend (.NET)

## Configurar conexión

Editar:

backend/appsettings.json

```
"ConnectionStrings": {
  "DefaultConnection": "Host=localhost;Database=bdproyecto;Username=postgres;Password=1234"
}
```

---

## Ejecutar API

```
cd backend
dotnet restore
dotnet run
```

Disponible en:

```
http://localhost:5000
```

Swagger:

```
http://localhost:5000/swagger
```

---

# 🔹 Frontend

Instalar dependencias (según stack):

Ejemplo:

```
cd frontend
npm install
npm start
```

o

```
python app.py
```

---

# 🔐 Autenticación

La API usa JWT.

Header requerido:

```
Authorization: Bearer <token>
```

---

# 📡 Endpoints principales (ejemplo)

## Usuarios
```
GET    /api/usuario
POST   /api/usuario
PUT    /api/usuario/{id}
DELETE /api/usuario/{id}
```

## Proyectos
```
GET    /api/proyecto
POST   /api/proyecto
PUT    /api/proyecto/{id}
DELETE /api/proyecto/{id}
```

## Actividades
```
GET    /api/actividad
POST   /api/actividad
PUT    /api/actividad/{id}
DELETE /api/actividad/{id}
```

## Presupuesto
```
GET    /api/presupuesto
GET    /api/ejecucion_presupuesto
GET    /api/distribucion_presupuesto
```

## Entregables
```
GET    /api/entregable
POST   /api/archivo_entregable
```

---

# 🗄️ Modelo de Base de Datos

Tablas principales:

- actividad
- archivo
- archivo_entregable
- distribucion_presupuesto
- ejecucion_presupuesto
- entregable
- estado
- estado_proyecto
- meta_estrategica
- meta_proyecto
- objetivo_estrategico
- presupuesto
- producto
- producto_entregable
- proyecto
- proyecto_producto
- responsable
- responsable_entregable
- tipo_producto
- tipo_proyecto
- tipo_responsable
- usuario
- variable_estrategia

---

# 🧪 Pruebas

Backend:

```
dotnet test
```



---

# 📄 Licencia

MIT
