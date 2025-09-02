# 📌 8 Sprints – Proyecto Supermercados

---

## 🚀 Sprint 1 – ⚙️ Setup e Infraestructura
**🎯 Objetivo:** Configurar el ambiente base.  
**✅ Entregables:**
- Docker Compose con FastAPI (backend), PostgreSQL (DB), Redis (cola), Worker, React (frontend), Mailhog.  
- Estructura de carpetas (`/api`, `/frontend`, `/worker`).  
- Endpoint `/health` para validar que el sistema responde.  

---

## 🚀 Sprint 2 – 🔐 Autenticación y Usuarios
**🎯 Objetivo:** Implementar login con roles.  
**✅ Entregables:**
- Endpoints `/auth/register` y `/auth/login`.  
- Roles: **Supermercado (Donante)**, **ONG (Receptor)** y **Administrador**.  
- Tokens JWT para seguridad.  
- Frontend: formularios de login y registro.  

---

## 🚀 Sprint 3 – 📦 Gestión de Donaciones (CRUD)
**🎯 Objetivo:** Registrar y listar donaciones de supermercados.  
**✅ Entregables:**
- Endpoint `POST /donations` (crear lote de alimentos con fecha de vencimiento, cantidad, ubicación).  
- Endpoint `GET /donations` (listar donaciones disponibles, filtro por vencimiento).  
- Base de datos con tabla `donations`.  
- Frontend: páginas **Registrar Donación** y **Ver Donaciones Disponibles**.  

---

## 🚀 Sprint 4 – 📍 Búsqueda por Ubicación y Urgencia
**🎯 Objetivo:** Permitir a ONGs encontrar donaciones cercanas y urgentes.  
**✅ Entregables:**
- Campos `lat`, `lng` en donaciones.  
- Filtro geográfico (ej. radio en km con fórmula Haversine o PostGIS).  
- Ordenar resultados por **fecha de vencimiento más próxima**.  
- Frontend: listado/mapa mostrando donaciones cercanas.  

---

## 🚀 Sprint 5 – 📝 Reservas de Alimentos
**🎯 Objetivo:** Permitir a ONGs reservar donaciones.  
**✅ Entregables:**
- Endpoint `POST /donations/{id}/reserve`.  
- Tabla `reservations` en PostgreSQL (estados: requested, confirmed, canceled).  
- Endpoint `GET /reservations` (listar reservas de cada ONG).  
- Frontend: botón **Reservar** y página **Mis Reservas**.  

---

## 🚀 Sprint 6 – ⏱️ Worker y Expiración Automática
**🎯 Objetivo:** Automatizar el ciclo de reservas.  
**✅ Entregables:**
- Worker con RQ (Redis) procesando tareas.  
- Expiración automática de reservas no confirmadas (ej. 30 minutos).  
- Reversión del estado del lote a “disponible”.  
- Notificación simulada (consola o Mailhog) a supermercado y ONG.  

---

## 🚀 Sprint 7 – 🔔 Notificaciones y Dashboard
**🎯 Objetivo:** Añadir métricas y comunicación.  
**✅ Entregables:**
- Notificaciones en eventos clave: creación de donación, reserva, expiración.  
- Endpoint `/me/dashboard` mostrando métricas según rol.  
- Frontend: dashboard con gráficos, por ejemplo:  
  - **Supermercado:** kg donados, % aprovechamiento, productos más donados.  
  - **ONG:** reservas activas, alimentos recibidos.  
  - **Admin:** métricas globales.  

---

## 🚀 Sprint 8 – 🏆 Demo Final y Optimización
**🎯 Objetivo:** Presentar el sistema completo funcionando.  
**✅ Entregables:**
- Flujo probado: **Supermercado registra alimentos → ONG reserva → Confirmación/Expiración → Dashboard actualizado**.  
- KPIs finales:  
  - % de alimentos entregados antes de vencimiento.  
  - Tasa de expiración de reservas.  
  - Tiempo promedio desde publicación hasta retiro.  
- Documentación completa y demo lista para socializar.  
