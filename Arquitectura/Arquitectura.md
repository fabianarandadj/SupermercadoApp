# 🧭 Arquitectura del Sistema

El sistema está diseñado bajo una **arquitectura modular distribuida**, separando responsabilidades en diferentes capas y servicios.

---

## 🔹 Frontend
- Desarrollado en **React (Vite)**.  
- Encargado de la interacción con los usuarios (**Supermercados, ONGs y Administradores**).  
- Incluye formularios para **login, registro de donaciones y reservas**, además de dashboards con métricas.  
- Se comunica con el backend a través de **API REST** sobre HTTPS, utilizando datos en formato **JSON**.  

---

## 🔹 Backend (API)
- Construido con **FastAPI (Python)**.  
- Expone los endpoints para **autenticación, gestión de usuarios, donaciones y reservas**.  
- Implementa **JWT** para la autenticación y control de roles (**Supermercado, ONG, Admin**).  
- Maneja la **lógica de negocio** principal del sistema.  

---

## 🔹 Base de Datos
- Se usa **PostgreSQL** como gestor relacional.  
- Almacena **usuarios, donaciones y reservas**.  
- Incluye relaciones entre supermercados (donantes), ONGs (receptoras) y los lotes de alimentos.  

---

## 🔹 Redis + Worker
- **Redis** funciona como caché y sistema de **cola de tareas**.  
- El **Worker (RQ)** procesa trabajos en segundo plano:  
  - Expira automáticamente las **reservas no confirmadas** después de cierto tiempo (ej. 30 minutos).  
  - Envía **notificaciones** (simuladas con Mailhog en desarrollo).  
  - Permite **escalar tareas asíncronas** sin sobrecargar la API.  

---

## 🔹 Mailhog (desarrollo)
- Herramienta que simula un servidor **SMTP**.  
- Permite probar el envío de **correos de confirmación, avisos de expiración y notificaciones** sin depender de un proveedor externo.  

---

## 🔹 Despliegue (Docker Compose)
- Todo el sistema se orquesta con **Docker Compose**.  
- Contenedores incluidos:  
  - `frontend` (React)  
  - `api` (FastAPI)  
  - `worker` (RQ)  
  - `postgres` (Base de Datos)  
  - `redis` (Cola/Cache)  
  - `mailhog` (Notificaciones de desarrollo)  
- Permite levantar el entorno completo con un solo comando:  
  ```bash
  docker-compose up
