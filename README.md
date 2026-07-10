# MS-Razas — Realm of Valyron

Microservicio de gestión de razas del proyecto RPG **Realm of Valyron**, desarrollado con Spring Boot 3.4.5 y desplegado en Render.

## Descripción

Este microservicio gestiona el catálogo de razas disponibles en el mundo RPG Realm of Valyron. Cada raza tiene atributos únicos que afectan las estadísticas de los personajes que la eligen.

## Tecnologías

- Java 21
- Spring Boot 3.4.5
- Spring Data JPA
- PostgreSQL (producción) / MySQL (desarrollo)
- Swagger / SpringDoc
- HATEOAS
- Docker

## Endpoints disponibles

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| GET | /api/v1/razas | Listar todas las razas |
| GET | /api/v1/razas/{id} | Obtener raza por ID |
| GET | /api/v1/razas?nombre={nombre} | Buscar raza por nombre |
| POST | /api/v1/razas | Crear nueva raza |
| PUT | /api/v1/razas/{id} | Actualizar raza |
| DELETE | /api/v1/razas/{id} | Eliminar raza |

## Documentación Swagger

Una vez desplegado, accede a la documentación interactiva en:

https://ms-razas.onrender.com/swagger-ui/index.html

## Ejecución local

```bash
# Clonar el repositorio
git clone https://github.com/joseignafm/ms-razas-render.git

# Ejecutar con perfil dev (requiere MySQL local)
./mvnw spring-boot:run -Dspring-boot.run.profiles=dev
```

## Variables de entorno (Render)

| Variable | Descripción |
|----------|-------------|
| DATABASE_URL | URL de conexión a PostgreSQL proporcionada por Render |
| PORT | Puerto asignado automáticamente por Render |

## Autor

Jose — Proyecto semestral Realm of Valyron
