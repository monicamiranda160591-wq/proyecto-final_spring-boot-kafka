# 📚Proyecto Final — Spring Boot & Kafka - E-commerce

Bienvenido al repositorio del proyecto **Spring Boot & Kafka - E-commerce**.  
Aquí encontrarás los enlaces a los microservicios relacionados y recursos adicionales.

---

## 📂 Microservicios del Proyecto

| Servicio | Descripción | Link |
|---------|-------------|------|
| 🛒 **ecommerce-product-service** | Gestión de productos del ecommerce | [Ir al repositorio](https://github.com/monicamiranda160591-wq/ecommerce-product-service) |
| 📦 **ecommerce-inventory-service** | Control de inventario y stock | [Ir al repositorio](https://github.com/monicamiranda160591-wq/ecommerce-inventory-service) |
| 📑 **ecommerce-order-service** | Gestión de órdenes y flujo de compra | [Ir al repositorio](https://github.com/monicamiranda160591-wq/ecommerce-order-service) |

---

## 🧪 Colección de Postman

Puedes encontrar la colección de Postman para probar los endpoints del sistema completo aquí:

👉 **[Descargar colección de Postman](./postman/proyecto-final_spring-boot-kafka.postman_collection.json)**

---

## 🔄 Arquitectura General

```mermaid
flowchart LR
    A[product-service] -->|Kafka topics| D[(Kafka)]
    B[inventory-service] -->|Kafka topics| D
    C[order-service] -->|Kafka topics| D
    D --> B
    D --> C
