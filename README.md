# Origami

## 🔎 Descripción  
Proyecto full-stack de e-commerce con backend en Java y Spring Boot, frontend en Vue.js/JavaScript/HTML5/Css3/Boostrap y base de datos embebida H2. Orientado a operaciones CRUD de productos/usuarios y funcionalidades típicas de tienda online. La arquitectura del proyecto es MVC (Modelo Vista Controlador), se uso JPA Hibernate para la persistir los datos.

## 🧠 Descripción general

Origami es una aplicación de comercio electrónico que permite:

Listar productos

Registrar y autenticar usuarios

Realizar operaciones de carrito y compras

Administrar catálogo desde el backend

El backend expone una API REST y el frontend consume estas rutas para mostrar la interfaz de usuario.


## 📁 Estructura del proyecto
```
origami/
├─ backend/                  # Spring Boot
│   ├─ src/main/java/
│   │   └─ com/.../configurations
|   |   └─ com/.../controllers
|   |   └─ com/.../DTOs
|   |   └─ com/.../Models
│   │   └─ com/.../repositories 
│   │   └─ com/.../services/
│   │   └─ com/.../utils
│   ├─ src/main/resources/
│   │   └─ application.properties
│   └─ build.gradle
├─ frontend/                 # Vue.js
│   ├─ src/main/resources/web
│   │   └─ assets/
│   │   └─ manager/
│   │   └─ pages/
└─ README.md
```


## 🧰 Tecnologías  
- Vue.js  
- JavaScript (ES6+)
- Gradle
- Java version 11
- Spring
- Spring Boot  
- Spring Security
- JPA
- Base de datos h2

## 🚀 Instalación y ejecución  
Asegúrate de tener Java 17+ y Gradle instalados.

En la raíz del proyecto:
```bash
# Clonar el repositorio  
git clone https://github.com/Josegtablante/origami.git
cd origami

# Ejecutar proyecto de forma local desde Intelli J
gradlew bootRun
http://localhost:8080/web/index.html

```
## 🚦 API Endpoints

## 🛍️ Productos

| Método | Ruta                 | Descripción                |
| ------ | -------------------- | -------------------------- |
| GET    | `/api/products`      | Obtener lista de productos |
| GET    | `/api/products/{id}` | Obtener producto por ID    |
| POST   | `/api/products`      | Crear nuevo producto       |
| PUT    | `/api/products/{id}` | Actualizar producto        |
| DELETE | `/api/products/{id}` | Eliminar producto          |


## 👤 Usuarios

| Método | Ruta                  | Descripción                       |
| ------ | --------------------- | --------------------------------- |
| POST   | `/api/users/register` | Registrar nuevo usuario           |
| POST   | `/api/users/login`    | Login de usuarios (autenticación) |
| GET    | `/api/users/{id}`     | Obtener perfil por ID             |


## 🧺 Carrito y compras

| Método | Ruta             | Descripción                   |
| ------ | ---------------- | ----------------------------- |
| GET    | `/api/cart`      | Obtener carrito del usuario   |
| POST   | `/api/cart`      | Agregar producto al carrito   |
| PUT    | `/api/cart/{id}` | Modificar cantidad en carrito |
| DELETE | `/api/cart/{id}` | Remover producto del carrito  |

## 🧩 Dependencias comunes (Spring Boot)

Estas dependencias suelen estar definidas en build.gradle para un proyecto como este.

dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-web'
    implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
    implementation 'com.h2database:h2'
    implementation 'org.springframework.boot:spring-boot-starter-security' // si tiene auth
    implementation 'org.springframework.boot:spring-boot-starter-validation'
    testImplementation 'org.springframework.boot:spring-boot-starter-test'
}

## 📦 Dependencias Frontend (Vue)

En package.json podría incluirse:

{
  "dependencies": {
    "vue": "^3.x",
    "vue-router": "^4.x",
    "axios": "^1.x"
  },
  "devDependencies": {
    "@vue/cli-service": "~5.x"
  }
}

