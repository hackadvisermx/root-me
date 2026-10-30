# Web - Client — Flash - Authentication

## Descripción

- **Reto:** [Root-Me — Flash - Authentication](https://www.root-me.org/en/Challenges/Web-Client/Flash-Authentication)

La comprobación de autenticación se realiza del lado del cliente dentro del recurso Flash, por lo que la lógica y el dato de comparación pueden revisarse sin depender de un control de acceso del servidor.

## Solución

1. Descargar el recurso Flash publicado por la instancia autorizada.
2. Inspeccionar su lógica de autenticación y la comparación de entrada del cliente.
3. Reproducir la entrada que satisface esa comprobación únicamente en la instancia del reto.
4. Usar el resultado exclusivamente en el formulario de validación de Root-Me.

## Verificación

La técnica se reprodujo contra la instancia vigente. Root-Me confirmó la palomita y el «Like»; el valor de validación no se versiona.

## Notas adicionales

- Un cliente no debe contener secretos ni ser la autoridad de una decisión de autenticación.
- La validación de credenciales debe ocurrir en un servidor bajo control de la aplicación.
