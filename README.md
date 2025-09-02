# 📌 Plan de 8 Sprints – Sistema Web de Aprovechamiento Social de Alimentos (Supermercados)

Este plan divide el proyecto en 8 sprints semanales.  
Cada sprint tiene un 🎯 **objetivo** y ✅ **entregables** claros para mostrar avances constantes.  

---

## 🚀 Sprint 1 – ⚙️ Setup e Infraestructura
**🎯 Objetivo:** Dejar lista la base tecnológica del sistema.  
**✅ Entregables:**
- Docker Compose con FastAPI (backend), PostgreSQL (DB), Redis (cola), Worker, React (frontend) y Mailhog.  
- Organización del proyecto (`/api`, `/frontend`, `/worker`).  
- Endpoint `/health` para validar funcionamiento inicial.  

---

## 🚀 Sprint 2 – 🔐 Autenticación y Usuarios
**🎯 Objetivo:** Gestionar usuarios con roles específicos.  
**✅ Entregables:**
- Endpoints `/auth/register` y `/auth/login`.  
- Roles: **Supermercado (Donante)**, **ONG (Receptor)** y **Administrador**.  
- Tokens JWT para autenticación.  
- Frontend: formularios de login y registro.  

---

## 🚀 Sprint 3 – 📦 Gestión de Donaciones (CRUD)
**🎯 Objetivo:** Permitir a supermercados registrar alimentos.  
**✅ Entregables:**
- Endpoint `POST /donations` (crear donación).  
- Endpoint `GET /donations` (listar con filtro por vencimiento).  
- Tabla `donations` en PostgreSQL.  
- Frontend: páginas **Registrar Donación** y **Ver Donaciones**.  

---

## 🚀 Sprint 4 – 📍 Búsqueda por Ubicación y Urgencia
**🎯 Objetivo:** Facilitar a ONGs encontrar donaciones cercanas y urgentes.  
**✅ Entregables:**
- Campos `lat`, `lng` en donaciones.  
- Filtro de radio (ej. 10 km) usando **Haversine o PostGIS**.  
- Ordenar resultados por **fecha de vencimiento**.  
- Frontend: lista/mapa con donaciones cercanas.  

---

## 🚀 Sprint 5 – 📝 Reservas de Alimentos
**🎯 Objetivo:** Permitir que ONGs reserven donaciones.  
**✅ Entregables:**
- Endpoint `POST /donations/{id}/reserve`.  
- Tabla `reservations` en PostgreSQL (estados: requested, confirmed, canceled).  
- Endpoint `GET /reservations` para ver reservas.  
- Frontend: botón **Reservar** y página **Mis Reservas**.  

---

## 🚀 Sprint 6 – ⏱️ Worker y Expiración Automática
**🎯 Objetivo:** Garantizar que los alimentos reservados no queden bloqueados.  
**✅ Entregables:**
- Worker con RQ procesando tareas en Redis.  
- Expiración automática de reservas no confirmadas en 30 minutos.  
- Reversión del estado de donación a “disponible”.  
- Notificación simulada en consola o Mailhog.  

---

## 🚀 Sprint 7 – 🔔 Notificaciones y Dashboard
**🎯 Objetivo:** Dar visibilidad y comunicación a todos los actores.  
**✅ Entregables:**
- Notificaciones en eventos clave: creación, reserva, expiración.  
- Endpoint `/me/dashboard` con métricas.  
- Frontend: dashboard con gráficos (ej. Recharts o Chart.js).  
- Métricas por rol:  
  - Supermercado: kg donados, % aprovechamiento, productos más donados.  
  - ONG: reservas activas, alimentos recibidos.  
  - Admin: métricas globales.  

---

## 🚀 Sprint 8 – 🏆 Demo Final y Optimización
**🎯 Objetivo:** Mostrar el sistema funcionando con un caso realista de supermercado → ONG.  
**✅ Entregables:**
- Flujo completo probado: **Supermercado registra alimentos → ONG reserva → Confirmación/Expiración → Dashboard**.  
- KPIs finales: % de alimentos entregados a tiempo, tasa de expiración, tiempo promedio de confirmación.  
- Documentación final y demo lista para socializar.  

---
