# Introducción

Proyecto laboral de práctica colaborativa que integra un frontend en Angular con un backend en Java Spring Boot, desarrollado durante la capacitación técnica en G&L Group.

## Descripción
Aplicación fullstack que separa la interfaz de usuario y la lógica de negocio en dos capas: frontend Angular para la experiencia del usuario y backend Spring Boot para las APIs, gestión de datos y reglas de negocio.

## Tecnologías
- Angular
- TypeScript
- Bootstrap
- PrimeNG
- Spring Boot
- Java 21
- Spring Data JPA
- MySQL
- Docker

## Estructura del proyecto
- `frontend/`: aplicación Angular con componentes, vistas y servicios para el cliente web construida con arquitectura de componentes
  - `src/app/`: lógica de la interfaz, componentes y rutas
  - `src/environments/`: configuración de entornos
  - `package.json`: scripts y dependencias del frontend
- `backend/`: servicio REST en Spring Boot construido con arquitectura hexagonal
  - `pom.xml`: dependencias y configuración de Maven
  - `src/main/java/`: código fuente del backend, controladores, entidades y casos de uso
  - `src/main/resources/application.properties`: configuración de Spring Boot
  - `src/test/java/`: pruebas unitarias y de integración
  - `Dockerfile`: imagen de Java para construir y ejecutar el servicio backend
  - `docker-compose.yml`: define el servicio MySQL y el backend usando el Dockerfile

## Ejecución
1. Clonar el repositorio
2. Levantar la base de datos y el backend con Docker Compose
   ```bash
   cd backend
   docker compose up -d
   ```
   Esto usa el `Dockerfile` del repositorio para construir el backend y también levanta el contenedor de MySQL definido en `docker-compose.yml`.
3. Iniciar el frontend Angular
   ```bash
   cd frontend
   pnpm install
   ng serve
   ```
   Si no se tiene `pnpm` instalado, se pueden ejecutar los comandos `npm install` y `npx ng serve`.

## Objetivos del proyecto
- Desarrollar una aplicación fullstack con frontend y backend separados
- Aplicar arquitecturas de diseño de software en Angular y Spring Boot
- Exponer APIs REST desde Java para consumo por la capa de interfaz
- Integrar componentes visuales y gráficos en el frontend
- Manejar validaciones y persistencia de datos en el backend