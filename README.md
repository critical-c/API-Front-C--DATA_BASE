# 📊 Sistema de Gestión de Proyectos

Aplicación web para la gestión y seguimiento de proyectos, actividades, presupuestos, entregables y responsables.

El sistema está dividido en:

- Backend: API REST en C# (.NET)
- Frontend: Python (Flask + Jinja)
- Base de datos: bdproyecto

Repositorio:
https://github.com/critical-c/API-Front-C--DATA_BASE.git

---

# 🚀 Funcionalidades

- Autenticación de usuarios
- Gestión de proyectos
- Gestión de actividades
- Control de presupuestos
- Ejecución presupuestal
- Gestión de entregables y archivos
- Asignación de responsables
- Estados de proyectos
- Arquitectura desacoplada (Frontend + API)

---

# 🧱 Arquitectura

Frontend (Flask)
      ↓
API REST (.NET C#)
      ↓
Base de Datos (bdproyecto)

---

# 🛠️ Tecnologías

## Backend
- C#
- ASP.NET Web API
- Entity Framework

## Frontend
- Python
- Flask
- Jinja2
- venv

## Base de datos
- PostgreSQL / SQL Server / MySQL

---

# 📂 Estructura del proyecto

```
API-Front-C--DATA_BASE/
│
├── API.NET C#/          # Backend .NET (API REST)
├── front/               # Frontend Flask + Jinja
├── bdproyecto.backup    # Respaldo de la base de datos
└── .gitignore
```

---

# ⚙️ Instalación y ejecución

## 1️⃣ Clonar repositorio

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

Puedes restaurar usando el archivo:

```
bdproyecto.backup
```

Ejemplo PostgreSQL:

```
pg_restore -U postgres -d bdproyecto bdproyecto.backup
```

---

# 🔹 Ejecutar Backend (.NET API)

Entrar a la carpeta:

```
cd "API.NET C#"
```

Restaurar dependencias:

```
dotnet restore
```

Ejecutar:

```
dotnet run
```

La API estará en:

```
http://localhost:5000
```

Swagger (si está activo):

```
http://localhost:5000/swagger
```

---

# 🔹 Ejecutar Frontend (Flask)

Entrar a la carpeta:

```
cd front
```

Crear entorno virtual:

```
python -m venv venv
```

Activar:

### Windows
```
venv\Scripts\activate
```

### Linux/Mac
```
source venv/bin/activate
```

Instalar dependencias:

```
pip install -r requirements.txt
```

Ejecutar:

```
python app.py
```

Disponible en:

```
http://localhost:3000
```

---

# 🔐 Autenticación

La API usa JWT.

Cada petición protegida debe enviar:

```
Authorization: Bearer <token>
```

---

# 📡 Módulos principales

- Usuario
- Proyecto
- Actividad
- Presupuesto
- Ejecución presupuestal
- Entregables
- Archivos
- Responsables
- Estados

---

# 🗄️ Tablas principales

- proyecto
- actividad
- presupuesto
- ejecucion_presupuesto
- distribucion_presupuesto
- entregable
- archivo
- responsable
- usuario
- estado
- producto
- meta_estrategica
- objetivo_estrategico
- variable_estrategia
- tipos y relaciones auxiliares



# 📄 Licencia

MIT
