# 🧾 Sistema de Facturación para Proveedor de Internet

Este proyecto consiste en un **sistema de facturación** orientado a un negocio proveedor de internet.  
El sistema permite gestionar clientes y generar facturas con diferentes conceptos: abonos (planes de internet), productos adicionales y cobros mensuales.

## 🚀 Tecnologías
- **Lenguaje:** JavaScript (Node.js)
- **Framework:** NestJS 
- **Base de datos:** PostgreSQL (dockerizada)
- **ORM recomendado:** Prisma ORM
- **Contenedores:** Docker + Docker Compose

## 📌 Entidades principales

- **Clientes**  
  Datos de los clientes (nombre, apellido, DNI, dirección).
- **Facturas**  
  Documento que reúne la información de pago: abonos, productos adicionales, datos del negocio y cliente.
- **Abonos**  
  Planes de internet ofrecidos por el negocio, con precio y características (CRUD).

### En primera instancia no estara aplicado, solo me centrare en los clientes con abonos mensulares.
- **Productos**  
  Ítems adicionales que el cliente puede comprar (equipos, accesorios, etc.).

## 📂 Endpoints (MVP inicial)

En esta primera versión solo se implementará el **CRUD de clientes y la solicitud de una factura**.

### Clientes (`/api/clientes`)

- **GET /api/clientes**  
  → Lista todos los clientes.

- **GET /api/clientes/:id**  
  → Obtiene un cliente por ID.

- **POST /api/clientes**  
  → Crea un nuevo cliente.  
   **Body ejemplo**:
  ```json
  {
    "nombre": "Ana",
    "apellido": "Gómez",
    "dni": "98765432",
    "cuil": "20-98765432-1",
    "direccion": "Av. Libertador 456"
  }

- **PUT /api/clientes/:id**
  → Actualiza un cliente existente.

- **DELETE /api/clientes/:id**
  → Elimina un cliente.

- **GET /api/facturas/:cuil**
  → Obtiene una factura por CUIL.

###  📈 Futuras mejoras
- Implementar endpoints para Facturas, Abonos y Productos.
- Autenticación con JWT.
- Frontend para gestión visual.
- Reportes en PDF de facturas.
- Facturacion electronica con AFIP
