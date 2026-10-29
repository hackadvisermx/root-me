# Web - Server — JWT - Unsecure Key Handling

## Descripción

- **Puntos:** 35
- **Reto:** [Root-Me — JWT - Unsecure Key Handling](https://www.root-me.org/en/Challenges/Web-Server/JWT-Unsecure-Key-Handling)

El encabezado JWT `kid` selecciona material de verificación sin limitarlo a claves conocidas. Un traversal puede hacer que el validador cargue un archivo local de contenido predecible como secreto HMAC.

## Solución

1. Conservar el algoritmo y canal de transporte del JWT legítimo entregado por la instancia.
2. Cambiar `kid` a una ruta traversal que apunte a un archivo local de contenido conocido, por ejemplo un archivo vacío predecible.
3. Ajustar únicamente el *claim* de privilegio requerido y firmar `header.payload` con el material conocido elegido por `kid`.
4. Enviar el JWT por el mismo canal original y usar la respuesta solo en Root-Me.

## Estado de revalidación

El vector `kid` fue identificado desde documentación específica del reto. Falta iniciar la instancia Start autenticada para confirmar la ruta permitida, reproducir el token, validar y registrar el «Like».

## Notas adicionales

- `kid` debe ser un identificador opaco y validarse contra una lista de claves permitidas.
- Los verificadores no deben resolver rutas del sistema desde entradas del token.
- La respuesta no se versiona.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/JWT-Unsecure-Key-Handling)
- [RFC 8725 — JSON Web Token Best Current Practices](https://www.rfc-editor.org/rfc/rfc8725)
