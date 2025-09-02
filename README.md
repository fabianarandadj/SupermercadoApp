## Sistema Web para el Control y Aprovechamiento Social de Alimentos Próximos a Vencer

## 👥 Integrantes
- Pedro Pablo Paque  
- Tito Fabian Aranda  
- Carlos Daniel Culma  

---

## 📖 Resumen
En Colombia se pierden anualmente cerca de **9,76 millones de toneladas de alimentos** (34 % de la producción nacional), lo que impacta la **seguridad alimentaria, la economía y el medio ambiente**.  
Mientras tanto, más de la mitad de la población vive en inseguridad alimentaria, y toneladas de alimentos aptos se pierden por vencimientos, ineficiencias logísticas o falta de redistribución.  

Este sistema busca **articular supermercados, fruterías, tiendas de barrio y organizaciones sociales**, mediante una plataforma web que:  
- Registra productos próximos a vencer.  
- Genera alertas automáticas.  
- Facilita la venta anticipada a bajo costo.  
- Promueve la donación a poblaciones vulnerables.  

---

## ❗ Planteamiento del Problema
El **34 % de la producción nacional** se desperdicia por falta de sistemas de control y redistribución.  
Esto genera **pérdidas económicas, impacto ambiental** y **agrava la inseguridad alimentaria** de millones de personas.  

---

## ✅ Justificación
- **Social:** Aporta a la seguridad alimentaria mediante donaciones oportunas, en cumplimiento de la **Ley 1990 de 2019**.  
- **Económica:** Reduce pérdidas en supermercados con alertas y ventas anticipadas.  
- **Ambiental:** Disminuye desperdicios y emisiones asociadas.  

---

## 🎯 Objetivos

### Objetivo General
Diseñar e implementar un **sistema web** para reducir el desperdicio de alimentos próximos a vencer, mediante:  
- Registro de inventarios.  
- Alertas automáticas.  
- Redistribución hacia poblaciones vulnerables.  

### Objetivos Específicos
- Diagnosticar causas de desperdicio en supermercados y fruterías.  
- Diseñar la arquitectura del sistema (frontend, backend, BD).  
- Implementar un repositorio digital para clasificación de alimentos.  
- Desarrollar notificaciones que alerten **7 y 5 días antes** del vencimiento.  

---

## 📚 Marco Teórico y Contexto
- En Colombia se pierden **9,76 millones de toneladas de alimentos/año** (34 % de la producción).  
- El desperdicio contribuye al **10 % de las emisiones de gases de efecto invernadero**.  
- La **Ley 1990 de 2019** exige donar alimentos próximos a vencer.  
- Ejemplos de referencia: **EatCloud** y **Corabastos**.  

---

## 🛠️ Metodología
Se usará un enfoque ágil basado en **Scrum**, adaptado a sprints semanales para garantizar avances continuos y entregables demostrables.

### Fases del trabajo
1. **Levantamiento de requisitos:** identificación de necesidades en supermercados y ONGs.  
2. **Diseño de arquitectura:** definición del frontend (React), backend (FastAPI/Django), worker y base de datos (PostgreSQL).  
3. **Implementación incremental:** desarrollo en sprints de 1 semana con objetivos claros (setup, login, CRUD, reservas, worker, notificaciones, dashboard y demo final).  
4. **Pruebas y validación:** ejecución de pruebas unitarias, validación funcional con datos de ejemplo y retroalimentación.  
5. **Entrega y documentación:** presentación del flujo completo y entrega del informe final.  

### Artefactos de Scrum
- **Product Backlog:** lista de funcionalidades priorizadas.  
- **Sprint Backlog:** tareas semanales definidas en cada sprint.  
- **Daily Scrum (simulada):** revisión breve de avances y obstáculos.  
- **Sprint Review:** presentación del incremento semanal.  
- **Sprint Retrospective:** identificación de mejoras en cada ciclo.  

---

## 📌 Alcance del Proyecto
### Incluye:
- Sistema web accesible desde navegador.  
- Registro y control de productos con campos clave (fecha de vencimiento, cantidad, proveedor, estado).  
- Alertas automáticas:  
  - ⏳ 7 días antes → activar promociones.  
  - ⏳ 5 días antes → destinar a donación.  
- Reportes estadísticos de reducción de desperdicio.  
- Cumplimiento de la **Ley 1990 de 2019**.  

### No incluye (1ra fase):
- App móvil nativa.  
- Integración con ERP externos.  
- Logística de transporte de alimentos.  

---

## 📈 Impacto Esperado
- **Social:** reducción del hambre en poblaciones vulnerables.  
- **Económico:** menores pérdidas para supermercados.  
- **Ambiental:** reducción de desperdicio y emisiones.  

---

## 🔧 Recursos y Herramientas
- **Tecnológicos:** FastAPI/Django, React, PostgreSQL, Redis, Docker, Mailhog.  
- **Humanos:** Equipo de desarrollo (backend, frontend, QA).  
- **Financieros:** Infraestructura mínima en la nube/local.  

---

## 🏁 Conclusiones
-El sistema permitirá **reducir el desperdicio alimentario**, optimizar inventarios en supermercados y **contribuir a la seguridad alimentaria** en Colombia.  

-Se espera que el proyecto sirva como **modelo replicable** en otras ciudades del país.  
