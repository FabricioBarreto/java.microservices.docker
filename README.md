# Java Microservices

Este proyecto es una implementación de microservicios en Java que utiliza contenedores Docker para simplificar la ejecución y la gestión de servicios independientes. La arquitectura de microservicios permite construir aplicaciones escalables y flexibles al dividir la funcionalidad en servicios pequeños y autónomos.

## Características Principales

- **Java 17:** La aplicación está desarrollada utilizando Java 17, siguiendo las mejores prácticas.

- **Base de datos:** Se utiliza MySQL y Postgres para el almacenamiento de los datos.

- **Microservicios en Java:** La aplicación está compuesta por servicios Java independientes que se comunican entre sí, logrando una arquitectura modular y fácilmente escalable.

- **Contenedores Docker:** Cada microservicio se empaqueta en un contenedor Docker, facilitando la implementación, distribución y escalabilidad de la aplicación.

- **Gestión de dependencias con Maven:** Se utiliza Maven para gestionar las dependencias y construir la aplicación de manera eficiente.

- **Postman:** Se emplea Postman para verificar la funcionalidad de los endpoints.

---

## EndPoints

### Product
- **Add product:** `POST` "localhost:8081/api/product"
  Datos de prueba:
  ```json
  {
    "sku": "00002",
    "name": "PC Gamer 2",
    "description": "Best PC 2",
    "price": "200000",
    "status": true
  }
  
- **List all products:** `GET` "localhost:8081/api/product"

### Inventory
- **Is in stock:** `POST` "localhost:8083/api/inventory/in-stock"
  Datos de prueba:
  ```json
  {
      "id": "1",
      "sku": "000001",
      "price": 10.00,
      "quantity": 2
  }

- **Find by SKU:** `GET` "localhost:8083/api/inventory/{sku}"

### Order
- **Place order:** `POST` "localhost:8082/api/order"
  Datos de prueba:
  ```json
  {
    "orderItems": [
      {
        "sku": "000001",
        "price": "20.00",
        "quantity": 2
      }
    ]
  }

- **Get all orders:** `GET` "localhost:8082/api/order"
