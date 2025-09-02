# 📌 Product Backlog – Sistema Web para el Control y Aprovechamiento Social de Alimentos Próximos a Vencer

## 🟢 Épica 1: Gestión de Usuarios y Roles

### Historia de usuario 1.1
- **Como** supermercado  
- **Quiero** registrarme e iniciar sesión  
- **Para** gestionar mis donaciones  

✅ **Criterios de aceptación**:
- Registro/login con usuario y contraseña  
- Roles: Supermercado, ONG y Administrador  
- Autenticación con JWT (token de sesión)  

---

### Historia de usuario 1.2
- **Como** administrador  
- **Quiero** gestionar usuarios y roles  
- **Para** tener control del sistema  

✅ **Criterios de aceptación**:
- CRUD de usuarios  
- Asignación y edición de roles  

---

## 🟢 Épica 2: Donaciones de Supermercados

### Historia de usuario 2.1
- **Como** supermercado  
- **Quiero** registrar productos próximos a vencer  
- **Para** que puedan ser redistribuidos  

✅ **Criterios de aceptación**:
- Formulario con nombre del producto, cantidad, fecha de vencimiento, ubicación  
- Guardar en base de datos  

---

### Historia de usuario 2.2
- **Como** supermercado  
- **Quiero** ver un listado de mis donaciones activas e históricas  
- **Para** tener control de inventario  

✅ **Criterios de aceptación**:
- Lista filtrada por estado (disponible, reservado, entregado, vencido)  
- Posibilidad de editar o cancelar donaciones  

---

## 🟢 Épica 3: Búsqueda y Reservas de ONGs

### Historia de usuario 3.1
- **Como** ONG  
- **Quiero** buscar alimentos próximos a vencer en supermercados cercanos  
- **Para** solicitarlos  

✅ **Criterios de aceptación**:
- Filtro por fecha de vencimiento y distancia (radio en km)  
- Orden por prioridad (más próximos a vencer primero)  

---

### Historia de usuario 3.2
- **Como** ONG  
- **Quiero** reservar un lote de alimentos  
- **Para** asegurar que no se pierda  

✅ **Criterios de aceptación**:
- Reserva con tiempo límite (ej. 30 min)  
- Estados: requested, confirmed, canceled, expired  

---

## 🟢 Épica 4: Alertas y Worker

### Historia de usuario 4.1
- **Como** sistema  
- **Quiero** expirar automáticamente reservas no confirmadas  
- **Para** liberar los alimentos  

✅ **Criterios de aceptación**:
- Worker con Redis  
- Reserva pasa de “requested” a “expired” después del tiempo límite  

---

### Historia de usuario 4.2
- **Como** ONG  
- **Quiero** recibir notificaciones cuando una reserva caduque o se confirme  
- **Para** estar informada oportunamente  

✅ **Criterios de aceptación**:
- Notificación simulada (email/console/Mailhog)  

---

## 🟢 Épica 5: Dashboard y Reportes

### Historia de usuario 5.1
- **Como** supermercado  
- **Quiero** ver un dashboard con métricas  
- **Para** saber cuánto alimento doné o aproveché  

✅ **Criterios de aceptación**:
- KPIs: total donado, % entregado a tiempo, productos más donados  

---

### Historia de usuario 5.2
- **Como** administrador  
- **Quiero** ver métricas globales  
- **Para** evaluar el impacto social del sistema  

✅ **Criterios de aceptación**:
- KPIs globales: kg recuperados, % aprovechamiento, tasa de vencimiento  

---

## 📊 Priorización inicial
- **Alta prioridad (MVP):** Épicas 1, 2 y 3  
- **Media prioridad:** Épica 4 (worker + notificaciones)  
- **Baja prioridad:** Épica 5 (dashboard avanzado)  
