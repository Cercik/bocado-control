# Control Remoto de la Aplicación Bocado

Este archivo controla el estado de activación/desactivación de la aplicación.

## Configuración Actual

El archivo `app_config.json` contiene:
```json
{
  "active": true,
  "message": ""
}
```

## ✅ Activar la Aplicación

```json
{
  "active": true,
  "message": ""
}
```

## ❌ Desactivar la Aplicación

```json
{
  "active": false,
  "message": "Aplicación en mantenimiento. Estará disponible pronto."
}
```

## 📝 Ejemplos de Mensajes

### Mantenimiento
```json
{
  "active": false,
  "message": "Mantenimiento programado. Disponible el 1 de diciembre a las 8:00 AM."
}
```

### Licencia Expirada
```json
{
  "active": false,
  "message": "Su licencia ha expirado. Por favor, contacte al administrador."
}
```

### Actualización
```json
{
  "active": false,
  "message": "Actualización en proceso. Por favor, intente más tarde."
}
```

### Suspensión Temporal
```json
{
  "active": false,
  "message": "El servicio está temporalmente suspendido. Contacte con soporte."
}
```

## 🔄 Cómo Funciona

1. La aplicación verifica este archivo al iniciar
2. Realiza verificaciones periódicas cada 30 minutos
3. Si `active` es `false`, muestra pantalla de bloqueo con el mensaje configurado
4. Los cambios se reflejan automáticamente en todos los dispositivos

## ⚙️ Instrucciones

1. Edita el archivo `app_config.json` en GitHub
2. Cambia `"active"` a `true` o `false`
3. Agrega un mensaje personalizado en `"message"`
4. Guarda los cambios (commit)
5. Los dispositivos detectarán el cambio en máximo 30 minutos

## 🔒 Seguridad

- Mantén este repositorio privado para mayor seguridad
- Solo usuarios autorizados deben tener acceso de escritura
- El sistema tiene fail-safe: si hay error de red, la app sigue funcionando
