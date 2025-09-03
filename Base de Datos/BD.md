# 👥 Roles y Llaves en la Base de Datos

- **USUARIOS**  
  - PK: `id_usuario`  
  - Atributos: nombre, correo, contraseña, rol (`SUPERMERCADO | ONG | ADMIN`), estado.  
  - Relación: 1 usuario puede crear **donaciones**, administrar **establecimientos** y **organizaciones**.  

- **ESTABLECIMIENTOS**  
  - PK: `id_establecimiento`  
  - FK: `id_usuario` → USUARIOS  
  - Cada usuario puede tener varios establecimientos.  

- **ORGANIZACIONES (ONGs)**  
  - PK: `id_organizacion`  
  - FK: `id_usuario` → USUARIOS  
  - Cada usuario puede administrar varias ONGs.  

- **PRODUCTOS**  
  - PK: `id_producto`  
  - FK: `id_establecimiento` → ESTABLECIMIENTOS  
  - Los establecimientos registran productos con fechas de vencimiento.  

- **ALERTAS**  
  - PK: `id_alerta`  
  - FK: `id_producto` → PRODUCTOS  
  - FK opcional: `id_organizacion` → ORGANIZACIONES  
  - Se generan cuando un producto está próximo a vencer o en condiciones especiales.  

- **DONACIONES**  
  - PK: `id_donacion`  
  - FK: `id_usuario` → USUARIOS  
  - Registro de las donaciones creadas por cada usuario.  

---

- **Llaves primarias (PK):** identifican cada registro único.  
- **Llaves foráneas (FK):** conectan usuarios con sus establecimientos, ONGs, productos, alertas y donaciones.  
