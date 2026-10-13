# API de viajes compartidos

API REST para una aplicación de **coche compartido** (al estilo BlaBlaCar), hecha con **Spring Boot**. Es un proyecto de la Universidad Politécnica de Madrid.

## Funcionalidades

- **Usuarios:** registro, login y cambio de contraseña.
- **Viajes:** crear, listar (con paginación), consultar y cancelar viajes.
- **Reservas:** reservar plazas en un viaje, consultar reservas y cancelarlas (con devolución).
- **Reseñas:** valorar a otros usuarios tras un viaje.

Los pagos y las notificaciones están simulados (`PagosFake`, `NotificacionesFake`).

## Estructura

```
src/main/java/es/upm/fi/grupo_i/
├── controller/   # Endpoints REST
├── service/      # Lógica de negocio
├── repository/   # Acceso a datos (JPA)
├── model/        # Entidades
├── dto/          # Objetos de entrada/salida de la API
├── mapper/       # Conversión entidad <-> DTO
└── enums/        # Estados de viaje/reserva, divisas...
```

## Cómo ejecutarlo

```bash
./mvnw spring-boot:run
```

Una vez arrancada:
- **Swagger UI:** http://localhost:8080/swagger-ui/index.html, para probar todos los endpoints
- **Consola H2:** http://localhost:8080/h2-console (JDBC URL `jdbc:h2:mem:grupoidb`, usuario `sa`, sin contraseña)

Para lanzar los tests:
```bash
./mvnw test
```

## Autores

- Jia Jie Ye – [L0stFr0mLighT]
- Yurong Cheng - [Yurong0q]
- Álvaro Vicente – [AlvaroVicente28]
