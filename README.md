# Restaurants Service - GastroReview

Microservicio REST con seguridad JWT para gestión de restaurantes y platillos.

## 🚀 Tecnologías

- Java 21
- Spring Boot 3.3.3
- Spring Security + JWT
- Spring Data JPA
- PostgreSQL (Neon)
- Spring Cloud Netflix Eureka Client
- Spring Cloud OpenFeign
- Maven

## 📦 Compilar

```bash
mvn clean package -DskipTests
```

## ▶️ Ejecutar Localmente

```bash
mvn spring-boot:run
```

## 🌐 Puerto

Este servicio corre en el puerto **8082**.

## 🔧 Configuración para Render

### Build Command
```
mvn clean package -DskipTests
```

### Start Command
```
java -jar target/*.jar
```

### Variables de Entorno
```
DATABASE_URL=jdbc:postgresql://ep-crimson-waterfall-a5g2m7gj.us-east-2.aws.neon.tech:5432/neondb?sslmode=require
DATABASE_USERNAME=neondb_owner
DATABASE_PASSWORD=npg_VkPsxdU17tEG
EUREKA_CLIENT_SERVICEURL_DEFAULTZONE=https://gastroreview-eureka.onrender.com/eureka/
JWT_SECRET=mySecretKeyForJWTTokenGenerationThatIsAtLeast256BitsLong
JAVA_OPTS=-Xmx512m -Xms256m
PORT=8082
```

## 🍽️ Endpoints Principales

- `GET /api/restaurants` - Listar restaurantes
- `GET /api/restaurants/{id}` - Obtener restaurante por ID
- `POST /api/restaurants` - Crear restaurante
- `PUT /api/restaurants/{id}` - Actualizar restaurante
- `GET /api/dishes` - Listar platillos
- `POST /api/dishes` - Crear platillo

## 📊 Base de Datos

Tablas gestionadas:
- `restaurants`
- `dishes`
- `addresses`
- `restaurant_images`
- `restaurant_categories`

## 🔗 Comunicación

- Usa Feign Client para comunicarse con Users Service

## 📝 Notas

- Requiere conexión a PostgreSQL (Neon)
- Implementa seguridad JWT
- Se registra automáticamente en Eureka
- Comunica con otros servicios vía Feign

## 🔗 Enlaces

- [Spring Cloud OpenFeign](https://spring.io/projects/spring-cloud-openfeign)
- [Spring Data JPA](https://spring.io/projects/spring-data-jpa)
