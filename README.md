# servidores-actividad3
API CRUD de Posts con un nuevo modelo de User exponiendo endpoints para login y agregando middlewares de autenticación.

# Tecnologías
Node.js, Express.js y Mongoose.

# npm install
Instala las dependencias y librerías requeridas.

# npm start
Levanta el API en el puerto 8000.

# Diseño modelo User
Diseño y programación de un modelo Mongoose "User" con los siguientes campos y validaciones en su esquema:
- name, string, requerido
- email, string, requerido, formato email
- password, string, requerido.
- bio, string
- active: boolean. Default false
- createdAt: Date
- updatedAt: Date

# API HTTP
Codifica los siguientes endpoints HTTP sobre el API:

# POST /api/users
- Recibe body JSON con los campos name, email, password y bio.
- Almacena el usuario en Base de Datos en memoria cifrando su contraseña.

# POST /api/login
- Recibe body con email, password
- Devuelve HTTP 200 OK con token JWT de sesión si las credenciales son correctas.
- Devuelve HTTP 400 en caso de error en la validación de datos.
- Devuelve HTTP 401 si las credenciales no son correctas.

El resto de endpoints de nuestra API (CRUD de Posts) tienen autenticación y devuelven código HTTP 401 ante peticiones no autenticadas.

# Utiliza un cliente HTTP cómo POSTMAN para hacer pruebas de peticiones a los diferentes endpoints.
