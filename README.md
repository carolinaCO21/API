# 📦 API – Tiendas y Empleados

**Base URL (producción):**
[https://apit2.vercel.app/](https://apit2.vercel.app/)

**Base URL (local):**
[http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🔐 Autenticación

La API utiliza **Bearer Token** para proteger las rutas de **Tiendas** y **Empleados**.

### Endpoints de autenticación

| Método | Ruta        | Descripción                    |
| ------ | ----------- | ------------------------------ |
| POST   | `/register` | Registrar un nuevo usuario     |
| POST   | `/login`    | Iniciar sesión y obtener token |

### Uso del token

El token debe enviarse en el header:

```http
Authorization: Bearer <token>
```

---

## 🏬 Rutas de TIENDAS

> Todas las rutas requieren autenticación Bearer Token

| Método | Ruta               | Descripción                   |
| ------ | ------------------ | ----------------------------- |
| GET    | `/tiendas/`        | Obtener todas las tiendas     |
| GET    | `/tiendas?id={id}` | Obtener tienda por ID (query) |
| GET    | `/tiendas/{id}`    | Obtener tienda por ID (path)  |
| POST   | `/tiendas/`        | Crear nueva tienda            |
| PUT    | `/tiendas/{id}`    | Modificar tienda completa     |
| PATCH  | `/tiendas/{id}`    | Actualizar campos específicos |
| DELETE | `/tiendas/{id}`    | Eliminar tienda               |

---

## 👷 Rutas de EMPLEADOS

> Todas las rutas requieren autenticación Bearer Token

| Método | Ruta                 | Descripción                     |
| ------ | -------------------- | ------------------------------- |
| GET    | `/empleados/`        | Obtener todos los empleados     |
| GET    | `/empleados?id={id}` | Obtener empleado por ID (query) |
| GET    | `/empleados/{id}`    | Obtener empleado por ID (path)  |
| POST   | `/empleados/`        | Crear nuevo empleado            |
| PUT    | `/empleados/{id}`    | Modificar empleado completo     |
| PATCH  | `/empleados/{id}`    | Actualizar campos específicos   |
| DELETE | `/empleados/{id}`    | Eliminar empleado               |

---

## 📝 Notas

* Todas las rutas de **Tiendas** y **Empleados** requieren autenticación.
* El token debe enviarse en cada request protegido.
* Los métodos `PUT` reemplazan el recurso completo.
* Los métodos `PATCH` actualizan solo los campos enviados.

---

## 🚀 Ejemplo de request

```bash
curl -X GET https://apit2.vercel.app/tiendas/ \
  -H "Authorization: Bearer <token>"
```

