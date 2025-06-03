# Microservicios - Catálogo de Productos

Este repositorio contiene tres microservicios desarrollados en Spring Boot que forman parte de un sistema de catálogo de productos:

- **ms-product**: gestión de productos y categorías.
- **ms-inventory**: gestión de stock de productos.
- **catalog-bff**: backend for frontend, encargado de orquestar y exponer los datos combinados a los clientes.

---

## 🔧 Requisitos

- Java 21
- Docker
- Postman
- IntelliJ / VSCode

---

## 📦 Estructura del proyecto

```
repo-bootcamp-microservicios-java/
├── catalog-bff/
├── ms-product/
├── ms-inventory/
└── README.md
```

---

## 🚀 Cómo levantar los servicios

Cada microservicio es independiente y puede levantarse desde su propia carpeta.


### ▶️ 2. Levantar servicios

Desde la raíz de cada microservicio:

```bash
cd ms-product
./mvnw spring-boot:run
```

```bash
cd ms-inventory
./mvnw spring-boot:run
```

```bash
cd catalog-bff
./mvnw spring-boot:run
```

O bien abrilos con tu IDE y ejecutalos desde `main()`.

---

## 🧪 Endpoints principales

| Servicio       | Swagger UI                            | OpenAPI YAML                        |
|----------------|----------------------------------------|-------------------------------------|
| `ms-product`   | http://localhost:8082/swagger-ui.html   | http://localhost:8082/v3/api-docs.yaml |
| `ms-inventory` | http://localhost:8081/swagger-ui.html   | http://localhost:8081/v3/api-docs.yaml |
| `catalog-bff`  | http://localhost:8080/swagger-ui.html   | http://localhost:8080/v3/api-docs.yaml |

---

## 📝 Notas

- El BFF orquesta llamadas a `ms-product` y `ms-inventory` para devolver productos con stock y categoría.
- Todos los servicios están protegidos por autenticación básica (`Basic Auth`).
- Podés usar los archivos `swagger.yaml` para documentación, compartir o generar clientes con OpenAPI Generator.

---

## ✨ Autor
- Leonardo Joaquin Morales. 
- Bootcamp Backend Java.
