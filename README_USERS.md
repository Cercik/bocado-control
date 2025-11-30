# Gestión de Usuarios

Este archivo controla el acceso a la aplicación de Comedor.

## Formato

```json
{
  "users": [
    {
      "username": "nombreusuario",
      "password": "contraseña",
      "role": "admin|user",
      "nombre": "Nombre Completo"
    }
  ]
}
```

## Usuarios Actuales

- **Admin** (Administrador principal)

## Agregar Usuario

Para agregar un nuevo usuario, edita `users.json` y agrega una entrada al array:

```json
{
  "username": "nuevo_usuario",
  "password": "contraseña_segura",
  "role": "user",
  "nombre": "Nombre del Usuario"
}
```

## Eliminar Usuario

Elimina la entrada del usuario del array `users`.

## Cambiar Contraseña

Modifica el campo `password` del usuario correspondiente.

## Notas de Seguridad

⚠️ **Importante**: Este sistema es básico. Las contraseñas están en texto plano en GitHub (repositorio público). Para un entorno de producción real, se recomienda:
- Usar autenticación con hash
- Almacenar credenciales en base de datos segura
- Implementar tokens de sesión
- Usar HTTPS para todas las comunicaciones
