# API
Tiendas y Empleados
https://apit2.vercel.app/

📍 Rutas de TIENDAS (todas requieren autenticación Bearer Token):
Base URL: http://127.0.0.1:8000

Método	Ruta	Descripción
GET	/tiendas/	Obtener todas las tiendas
GET	/tiendas?id={id}	Obtener tienda por ID (query)
GET	/tiendas/{id}	Obtener tienda por ID (path)
POST	/tiendas/	Crear nueva tienda
PUT	/tiendas/{id}	Modificar tienda completa
PATCH	/tiendas/{id}	Actualizar campos específicos
DELETE	/tiendas/{id}	Eliminar tienda
📍 Rutas de EMPLEADOS (todas requieren autenticación Bearer Token):
Método	Ruta	Descripción
GET	/empleados/	Obtener todos los empleados
GET	/empleados?id={id}	Obtener empleado por ID (query)
GET	/empleados/{id}	Obtener empleado por ID (path)
POST	/empleados/	Crear nuevo empleado
PUT	/empleados/{id}	Modificar empleado completo
PATCH	/empleados/{id}	Actualizar campos específicos
DELETE	/empleados/{id}	Eliminar empleado
🔐 Autenticación:
Método	Ruta	Descripción
POST	/register	Registrar nuevo usuario
POST	/login	Iniciar sesión y obtener token
Nota: Todas las rutas de tiendas y empleados requieren el token en el header Authorization: Bearer <token>
