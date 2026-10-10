# Mobile API - Spring Boot & JWT Authentication

Una API RESTful desarrollada con **Java** y **Spring Boot**, diseñada para gestionar la autenticación y autorización segura de usuarios mediante **JSON Web Tokens (JWT)** y **Spring Security**.

---

## 🚀 Características Principal

* **Autenticación con JWT**: Generación y validación de tokens de acceso para proteger rutas de la aplicación.
* **Spring Security**: Configuración de seguridad avanzada para la gestión de solicitudes y permisos.
* **Arquitectura Limpia**: Separación clara de responsabilidades con controladores, servicios y configuraciones dedicadas.
* **Maven Wrapper**: Incluido para facilitar la compilación y ejecución del proyecto sin depender de una instalación local de Maven.

---

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** Java 17+
* **Framework:** Spring Boot
* **Seguridad:** Spring Security, io.jsonwebtoken (jjwt)
* **Gestor de Dependencias:** Maven
* **Construcción:** Maven Wrapper (`mvnw`)

---

## 📂 Estructura del Proyecto

```text
mobileapi/
├── src/
│   ├── main/
│   │   ├── java/com/mobile/api/
│   │   │   ├── config/
│   │   │   │   └── SecurityConfig.java         # Configuración general de Spring Security
│   │   │   ├── controller/
│   │   │   │   └── AuthController.java         # Endpoints de autenticación (Login/Register)
│   │   │   ├── security/
│   │   │   │   ├── JwtAuthenticationFilter.java# Filtro para interceptar y validar tokens
│   │   │   │   └── JwtService.java             # Lógica para generación y lectura de JWT
│   │   │   └── MobileapiApplication.java       # Punto de entrada de la aplicación
│   │   └── resources/
│   │       └── application.properties          # Propiedades de la aplicación
│   └── test/                                   # Pruebas unitarias y de integración
├── .gitignore
├── pom.xml                                     # Dependencias y configuración de Maven
└── README.md
```

---

## 🔑 Endpoints de la API

| Método | Endpoint | Descripción | Acceso |
| :--- | :--- | :--- | :--- |
| `POST` | `/api/v1/auth/register` | Registro de nuevo usuario | Público |
| `POST` | `/api/v1/auth/login` | Autenticación de usuario y obtención del JWT | Público |
| `GET` | `/api/v1/demo` | Endpoint de prueba protegido | Requiere Token (`Bearer <JWT>`) |

---

## ⚙️ Configuración y Ejecución Local

### Prerrequisitos

* **Java JDK 17** o superior instalado.
* Git instalado en tu máquina.

### Pasos para ejecutar

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/edrandededraalr2-tech3/rest_ap_ijwt.git
   cd rest_ap_ijwt
   ```

2. **Compilar el proyecto:**
   ```bash
   ./mvnw clean package
   ```

3. **Ejecutar la aplicación:**
   ```bash
   ./mvnw spring-boot:run
   ```

La API estará disponible por defecto en `http://localhost:8080`.

---

## 🧪 Pruebas de Autenticación

Para consumir rutas protegidas, incluye el token JWT en el encabezado (Header) de la solicitud HTTP:

```http
Authorization: Bearer <TU_TOKEN_JWT>
```

---

## ✒️ Autor

Desarrollado por **[edrandededraalr2-tech3](https://github.com/edrandededraalr2-tech3)**.